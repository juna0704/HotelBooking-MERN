// BASIC APP
/\*
import express, { Request, Response } from 'express';
import cors from 'cors';
import 'dotenv/config';

const app = express();
app.use(express.json());
app.use(express.urlencoded({ extended: true }));
app.use(cors());

app.get('/api/test', async (req: Request, res: Response) => {
res.json({ message: 'hello from express endpoint' });
});

app.listen(7000, () => {
console.log('server is running on localhost:7000');
});
\*/

created .env file in root dir
stored uri for mongodb in .env file
in index.ts file added these code for mongodb
/\*\ DATABASE CONNECTION
import mongoose from 'mongoose';

mongoose.connect(process.env.MONGODB_CONNECTION_STRING as string);

if (!process.env.MONGODB_CONNECTION_STRING) {
console.error(
'MONGODB_CONNECTION_STRING is not defined in the environment variables'
);
process.exit(1);
}

mongoose
.connect(process.env.MONGODB_CONNECTION_STRING)
.then(() => console.log('Connected to MongoDB'))
.catch((error) => {
console.error('MongoDB connection error:', error);
process.exit(1);
});
\*/

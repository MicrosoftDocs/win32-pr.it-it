---
description: In questa sezione viene descritto il formato dei record per ogni token di registrazione. Le informazioni sono suddivise nelle sezioni seguenti.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Record di token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456ee591f15cac6e6a3d2fecaad3dfca9f0709b39a63d20fe198e591a199f4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797423"
---
# <a name="token-records"></a>Record di token

In questa sezione viene descritto il formato dei record per ogni token di registrazione. Le informazioni sono suddivise nelle sezioni seguenti.

-   [NOME \_ TOKEN](/windows)
-   [STRINGA \_ TOKEN](/windows)
-   [TOKEN \_ INTEGER](/windows)
-   [TOKEN \_ GUID](/windows)
-   [ELENCO \_ DI TOKEN INTEGER \_](/windows)
-   [ELENCO \_ FLOAT \_ DEI TOKEN](/windows)

## <a name="token_name"></a>NOME \_ TOKEN

Record a lunghezza variabile. Il token è seguito da un valore count che specifica il numero di byte che seguono nel campo name. Il record viene completato da un nome ASCII di conteggio della lunghezza.



| Campo | Tipo       | Dimensioni (byte) | Contenuto                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | nome del \_ token                    |
| count | DWORD      | 4            | Lunghezza del campo del nome, in byte |
| name  | Matrice BYTE | count        | Nome ASCII                     |



 

## <a name="token_string"></a>STRINGA \_ TOKEN

Record a lunghezza variabile. Il token è seguito da un valore count che specifica il numero di byte che seguono nel campo stringa. Una stringa ASCII di conteggio della lunghezza continua il record, che viene completato da un token di terminazione. La scelta del carattere di terminazione è determinata dai problemi di sintassi illustrati altrove.



| Campo      | Tipo       | Dimensioni (byte) | Contenuto                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | stringa di \_ token                    |
| count      | DWORD      | 4            | Lunghezza del campo stringa in byte  |
| Stringa     | Matrice BYTE | count        | Stringa ASCII                     |
| Terminator | DWORD      | 4            | PUNTO E VIRGOLA TOKEN \_ o TOKEN \_ COMMA |



 

## <a name="token_integer"></a>TOKEN \_ INTEGER

Record a lunghezza fissa. Il token è seguito dal valore intero richiesto.



| Campo | Tipo  | Dimensioni (byte) | Contenuto       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | tOKEN \_ INTEGER |
| Valore | DWORD | 4            | Intero singolo |



 

## <a name="token_guid"></a>TOKEN \_ GUID

Record a lunghezza fissa. Il token è seguito dai quattro campi dati definiti dallo standard DCE OSF.



| Campo | Tipo       | Dimensioni (byte) | Contenuto          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | GUID tOKEN \_       |
| Data1 | DWORD      | 4            | Campo dati UUID 1 |
| Dati2 | WORD       | 2            | Campo dati UUID 2 |
| Dati3 | WORD       | 2            | Campo dati UUID 3 |
| Dati4 | Matrice BYTE | 8            | Campo dati UUID 4 |



 

## <a name="token_integer_list"></a>ELENCO \_ DI TOKEN INTEGER \_

Record a lunghezza variabile. Il token è seguito da un valore count che specifica il numero di numeri interi che seguono nel campo dell'elenco. Per migliorare l'efficienza, gli elenchi di numeri interi consecutivi devono essere composti in un unico elenco.



| Campo | Tipo  | Dimensioni (byte) | Contenuto                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | TOKEN \_ INTEGER \_ LISt             |
| count | DWORD | 4            | Numero di numeri interi nel campo elenco |
| list  | DWORD | 4 x conteggio    | Elenco di numeri interi                     |



 

## <a name="token_float_list"></a>TOKEN \_ FLOAT \_ LIST

Record a lunghezza variabile. Il token è seguito da un valore count che specifica il numero di valori float o double che seguono nel campo dell'elenco. Le dimensioni del valore a virgola mobile (float o double) sono determinate dal valore di float sizespecificato nell'intestazione del file. Per migliorare l'efficienza, i TOKEN FLOAT LIST consecutivi \_ devono essere composti in un unico \_ elenco.



| Campo | Tipo               | Dimensioni (byte)   | Contenuto                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | tOKEN \_ FLOAT \_ LISt                        |
| count | DWORD              | 4              | Numero di valori float o double nel campo elenco |
| list  | Matrice float/double | 4 o 8 x conteggio | Elenco float o double                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica binaria](binary-encoding.md)
</dt> </dl>

 

 

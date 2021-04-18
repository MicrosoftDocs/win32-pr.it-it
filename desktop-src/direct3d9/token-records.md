---
description: In questa sezione viene descritto il formato dei record per ognuno dei token che portano a record. Le informazioni sono suddivise nelle sezioni riportate di seguito.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Record di token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304365"
---
# <a name="token-records"></a>Record di token

In questa sezione viene descritto il formato dei record per ognuno dei token che portano a record. Le informazioni sono suddivise nelle sezioni riportate di seguito.

-   [nome del TOKEN \_](/windows)
-   [\_stringa token](/windows)
-   [\_Integer token](/windows)
-   [\_GUID token](/windows)
-   [\_elenco di valori integer del token \_](/windows)
-   [\_elenco float del token \_](/windows)

## <a name="token_name"></a>nome del TOKEN \_

Record a lunghezza variabile. Il token è seguito da un valore Count che specifica il numero di byte che seguono nel campo Name. Un nome ASCII con numero di lunghezza completa il record.



| Campo | Tipo       | Dimensioni (byte) | Contenuto                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | nome del token \_                    |
| count | DWORD      | 4            | Lunghezza del campo del nome, in byte |
| name  | Matrice di BYTE | count        | Nome ASCII                     |



 

## <a name="token_string"></a>\_stringa token

Record a lunghezza variabile. Il token è seguito da un valore Count che specifica il numero di byte che seguono nel campo della stringa. Una stringa ASCII di lunghezza count continua il record, che viene completato da un token di terminazione. La scelta del carattere di terminazione è determinata dai problemi di sintassi descritti altrove.



| Campo      | Tipo       | Dimensioni (byte) | Contenuto                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | \_stringa token                    |
| count      | DWORD      | 4            | Lunghezza del campo stringa in byte  |
| Stringa     | Matrice di BYTE | count        | Stringa ASCII                     |
| terminazione | DWORD      | 4            | punto e virgola del tOKEN \_ o \_ virgola del token |



 

## <a name="token_integer"></a>\_Integer token

Record A lunghezza fissa. Il token è seguito dal valore Integer obbligatorio.



| Campo | Tipo  | Dimensioni (byte) | Contenuto       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | \_Integer tOKEN |
| Valore | DWORD | 4            | Singolo Integer |



 

## <a name="token_guid"></a>\_GUID token

Record a lunghezza fissa. Il token è seguito dai quattro campi dati definiti dallo standard OSF DCE.



| Campo | Tipo       | Dimensioni (byte) | Contenuto          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | \_GUID tOKEN       |
| Data1 | DWORD      | 4            | Campo dati UUID 1 |
| Data2 | WORD       | 2            | Campo dati UUID 2 |
| Data3 | WORD       | 2            | Campo dati UUID 3 |
| DATA4 | Matrice di BYTE | 8            | Campo dati UUID 4 |



 

## <a name="token_integer_list"></a>\_elenco di valori integer del token \_

Record a lunghezza variabile. Il token è seguito da un valore Count che specifica il numero di numeri interi che seguono nel campo dell'elenco. Per maggiore efficienza, gli elenchi di numeri interi consecutivi devono essere composti in un singolo elenco.



| Campo | Tipo  | Dimensioni (byte) | Contenuto                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | \_elenco di valori integer del tOKEN \_             |
| count | DWORD | 4            | Numero di numeri interi nel campo elenco |
| list  | DWORD | conteggio 4 x    | Elenco di numeri interi                     |



 

## <a name="token_float_list"></a>\_elenco float del token \_

Record a lunghezza variabile. Il token è seguito da un valore Count che specifica il numero di valori float o Double che seguono nel campo dell'elenco. Le dimensioni del valore a virgola mobile (float o Double) sono determinate dal valore di float SizeSpecified nell'intestazione del file. Per maggiore efficienza, gli \_ elenchi float di token consecutivi \_ devono essere composti in un singolo elenco.



| Campo | Tipo               | Dimensioni (byte)   | Contenuto                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | \_elenco float del tOKEN \_                        |
| count | DWORD              | 4              | Numero di valori float o Double nel campo elenco |
| list  | matrice float/double | conteggio 4 o 8 x | Elenco float o Double                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica binaria](binary-encoding.md)
</dt> </dl>

 

 

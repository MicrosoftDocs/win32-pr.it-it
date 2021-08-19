---
description: Gestione degli handle di file transazionali in NTFS transazionale.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Come usare NTFS transazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8daafd2bc2ee0e695ee3bdede4ac2f62be1000c111d0c544dec877c357f42629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015279"
---
# <a name="how-to-use-transactional-ntfs"></a>Come usare NTFS transazionale

## <a name="transacted-file-handles"></a>Handle di file transazione

NTFS transazionale (TxF) associa un handle di file a una transazione. Per le operazioni che funzionano su un handle (ad esempio, le funzioni [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile),**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) la chiamata di funzione API effettiva non cambia. Per le operazioni su file che accettano un nome, sono disponibili funzioni transazionche esplicite per queste operazioni. Ad esempio, invece di [**chiamare CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), chiamare [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda). Viene creato un handle di file transazione, che può quindi essere usato per tutte le operazioni sui file che richiedono un handle. Tutte le operazioni successive che usano questo handle sono operazioni transazionate.

## <a name="basic-txf-usage"></a>Utilizzo TxF di base

La serie di passaggi seguente rappresenta l'utilizzo più semplice per TxF. Sono supportati anche scenari più complessi, a discrezione della finestra di progettazione dell'applicazione.

1.  Creare una transazione chiamando la funzione [**KTM CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) o usando l'interfaccia **IKernelTransaction** [del Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC).
2.  Ottenere gli handle di file transazionati chiamando [**CreateFileTransacted.**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
3.  Modificare i file in base alle esigenze usando gli handle di file transazionati.
4.  Chiudere tutti gli handle di file transazione associati alla transazione creata nel passaggio 1.
5.  Eseguire il commit o interrompere la transazione chiamando la funzione KTM o DTC corrispondente.

## <a name="key-points-of-the-txf-programming-model"></a>Punti chiave del modello di programmazione TxF

Il modello di programmazione TxF presenta i punti chiave seguenti da considerare quando si sviluppa un'applicazione TxF:

-   È consigliabile che un'applicazione chieda tutti gli handle di file transazionale prima di eseguire il commit o il rollback di una transazione. Il sistema invalida tutti gli handle transazionale al termine di una transazione. Qualsiasi operazione, ad eccezione di close, eseguita su un handle transazionale al termine della transazione restituisce l'errore seguente: **ERROR HANDLE NO LONGER \_ \_ \_ \_ VALID**.
-   Un file viene visualizzato come un'unità di archiviazione. Sono supportati aggiornamenti parziali e sovrascrittura completa dei file. Più transazioni non possono modificare contemporaneamente lo stesso file.
-   L'I/O mappato alla memoria è trasparente e coerente con le normali I/O di file. Un'applicazione deve scaricare e chiudere una sezione aperta prima di eseguire il commit di una transazione. La mancata esecuzione di questa operazione può comportare modifiche parziali al file mappato all'interno della transazione. Se questa operazione non viene eseguita, il rollback ha esito negativo.

## <a name="common-programming-errors"></a>Errori di programmazione comuni

Quando si sviluppano applicazioni transazionate, possono verificarsi gli errori comuni seguenti:

-   Utilizzo di un handle di file dopo il completamento di una transazione.
-   Se non si chiudono handle a file e directory eliminati prima di eseguire il commit di una transazione, le operazioni di eliminazione non verranno eseguite. Questo evento deve verificarsi prima di eseguire il commit perché l'operazione di eliminazione venga considerata parte della transazione. Ciò è dovuto al fatto che il sistema non elimina effettivamente un file fino a quando non viene chiuso l'ultimo handle, anche quando l'operazione non viene eseguita in transazioni, come parte del sottosistema di I/O del file Windows.
-   Mancata considerazione dei rollback delle transazioni avviate dal sistema, che possono verificarsi in qualsiasi momento. Ad esempio, se le risorse di sistema sono esaurite, viene eseguito il rollback di una transazione.

 

 

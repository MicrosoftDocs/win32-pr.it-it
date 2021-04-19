---
description: Gestione degli handle di file transazionali in NTFS transazionale.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Come utilizzare Transactional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43681f0d5b27f0db03d8b6c44564b792fce4b467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317786"
---
# <a name="how-to-use-transactional-ntfs"></a>Come utilizzare Transactional NTFS

## <a name="transacted-file-handles"></a>Handle di file transazionali

Transactional NTFS (TxF) associa un handle di file a una transazione. Per le operazioni che funzionano su un handle (ad esempio, le funzioni [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ), la chiamata di funzione API effettiva non cambia. Per le operazioni sui file che accettano un nome, sono disponibili funzioni transazionali esplicite per queste operazioni. Ad esempio, invece di chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), chiamare [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda). Viene creato un handle di file transazionale, che può quindi essere usato per tutte le operazioni sui file che richiedono un handle. Tutte le operazioni successive che usano questo handle sono operazioni transazionali.

## <a name="basic-txf-usage"></a>Utilizzo TxF di base

La serie di passaggi seguente rappresenta l'utilizzo più semplice per TxF. Sono supportati anche scenari più complessi, a discrezione di progettazione applicazioni.

1.  Creare una transazione chiamando la funzione KTM [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) o usando l'interfaccia **IKernelTransaction** del [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC).
2.  Ottenere handle di file transazionali chiamando [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).
3.  Modificare i file in base alle esigenze usando gli handle di file transazionali.
4.  Chiudere tutti gli handle di file transazionali associati alla transazione creata nel passaggio 1.
5.  Eseguire il commit o interrompere la transazione chiamando la funzione KTM o DTC corrispondente.

## <a name="key-points-of-the-txf-programming-model"></a>Punti chiave del modello di programmazione TxF

Il modello di programmazione TxF presenta i punti chiave seguenti da considerare quando si sviluppa un'applicazione TxF:

-   Si consiglia vivamente che un'applicazione chiuda tutti gli handle di file transazionali prima di eseguire il commit o il rollback di una transazione. Il sistema invalida tutti gli handle transazionali al termine di una transazione. Qualsiasi operazione, eccetto Close, eseguita su un handle transazionale dopo la fine della transazione restituisce il seguente errore: l' **handle di errore \_ non è \_ \_ più \_ valido**.
-   Un file viene visualizzato come unità di archiviazione. Sono supportati gli aggiornamenti parziali e le sovrascritture di file completi. Più transazioni non possono modificare contemporaneamente lo stesso file.
-   L'I/O mappato alla memoria è trasparente e coerente con l'i/O dei file normali. Un'applicazione deve scaricare e chiudere una sezione aperta prima di eseguire il commit di una transazione. In caso contrario, è possibile che vengano apportate modifiche parziali al file mappato all'interno della transazione. Se questa operazione non viene eseguita, il rollback non riesce.

## <a name="common-programming-errors"></a>Errori comuni di programmazione

Durante lo sviluppo di applicazioni transazionali possono verificarsi gli errori comuni seguenti:

-   Utilizzando un handle di file dopo il completamento di una transazione.
-   Impossibile chiudere gli handle per i file e le directory eliminati prima di eseguire il commit di una transazione, in modo da impedire che si verifichino le operazioni di eliminazione. Questo evento deve verificarsi prima di eseguire il commit affinché l'operazione di eliminazione venga considerata parte della transazione. Questo perché il sistema non elimina effettivamente un file fino a quando non viene chiuso l'ultimo handle, anche quando l'operazione non è transazionale, come parte del sottosistema di I/O dei file di Windows.
-   Impossibile tenere conto dei rollback delle transazioni avviati dal sistema, che possono verificarsi in qualsiasi momento; Se, ad esempio, le risorse di sistema sono esaurite, viene eseguito il rollback di una transazione.

 

 

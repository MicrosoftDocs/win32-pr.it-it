---
description: Transactional NTFS (TxF) integra le transazioni nel file system NTFS, che consente agli sviluppatori e agli amministratori di applicazioni di gestire correttamente gli errori e di mantenere l'integrità dei dati.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Informazioni su Transactional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343641"
---
# <a name="about-transactional-ntfs"></a>Informazioni su Transactional NTFS

\[Microsoft consiglia vivamente agli sviluppatori di utilizzare metodi alternativi per soddisfare le esigenze dell'applicazione. Molti scenari in cui TxF è stato sviluppato possono essere realizzati attraverso tecniche più semplici e più facilmente disponibili. Inoltre, è possibile che TxF non sia disponibile nelle versioni future di Microsoft Windows. Per altre informazioni e per le alternative a TxF, vedere [alternative all'uso di Transactional NTFS](deprecation-of-txf.md).\]

Transactional NTFS (TxF) integra le transazioni nel file system NTFS, che consente agli sviluppatori e agli amministratori di applicazioni di gestire correttamente gli errori e di mantenere l'integrità dei dati.

TxF può partecipare alle transazioni distribuite coordinate da [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) , che consente di usare TXF per gli elementi seguenti:

-   Transazioni che si estendono su più archivi dati, ad esempio una singola transazione per le operazioni di file e SQL
-   Transazioni che si estendono su più computer, ad esempio una singola transazione per gli aggiornamenti di file in più computer

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                 | Descrizione                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Quando utilizzare Transactional NTFS](when-to-use-transactional-ntfs.md)<br/>                                       | Utilizzare Transactional NTFS per mantenere l'integrità dei dati.<br/>                                                                        |
| [Distribuzione di Transactional NTFS](deploying-transactional-ntfs.md)<br/>                                           | Controllo della memorizzazione nella cache in Transactional NTFS.<br/>                                                                                    |
| [Come utilizzare Transactional NTFS](how-to-use-transactional-ntfs.md)<br/>                                         | Gestione degli handle di file transazionali in NTFS transazionale.<br/>                                                                   |
| [Concetti di base di TxF](txf-basic-concepts.md)<br/>                                                               | Descrive la coerenza Read Committed, l'isolamento Read committed e i concetti di blocco transazionale in Transactional NTFS.<br/> |
| [Considerazioni sulla programmazione per Transactional NTFS](programming-considerations-for-transacted-fileio-.md)<br/> | Vengono descritte le varie considerazioni di programmazione per Transactional NTFS.<br/>                                                      |
| [Considerazioni sulle prestazioni per la funzionalità NTFS transazionale](performance-considerations-for-transactional-ntfs.md)<br/> | Suggerimenti per le transazioni file system ottimali.<br/>                                                                     |



 

 


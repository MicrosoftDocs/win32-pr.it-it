---
description: Transactional NTFS (TxF) integra le transazioni nel file system NTFS, semplificando la gestione degli errori e la conservazione dell'integrità dei dati da parte degli sviluppatori e degli amministratori delle applicazioni.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Informazioni su TRANSACTIONAL NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404dc966673eac9d61229ab127877941fe82354ddffcfd021ba76b9931c8e097
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102111"
---
# <a name="about-transactional-ntfs"></a>Informazioni su TRANSACTIONAL NTFS

\[Microsoft consiglia vivamente agli sviluppatori di usare mezzi alternativi per soddisfare le esigenze dell'applicazione. Molti scenari per cui È stato sviluppato TxF possono essere ottenuti con tecniche più semplici e più facilmente disponibili. Inoltre, TxF potrebbe non essere disponibile nelle versioni future di Microsoft Windows. Per altre informazioni e alternative a TxF, vedere [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]

Transactional NTFS (TxF) integra le transazioni nel file system NTFS, semplificando la gestione degli errori e la conservazione dell'integrità dei dati da parte degli sviluppatori e degli amministratori delle applicazioni.

TxF può partecipare a transazioni distribuite coordinate dal Distributed Transaction Coordinator [(DTC),](/previous-versions/windows/desktop/ms684146(v=vs.85)) che consente di usare TxF per gli elementi seguenti:

-   Transazioni che si estendono su più archivi dati, ad esempio una singola transazione per operazioni su file SQL dati
-   Transazioni che si estendono su più computer, ad esempio una singola transazione per gli aggiornamenti di file in più computer

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                 | Descrizione                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Quando usare NTFS transazionale](when-to-use-transactional-ntfs.md)<br/>                                       | Usare NTFS transazionale per mantenere l'integrità dei dati.<br/>                                                                        |
| [Distribuzione di NTFS transazionale](deploying-transactional-ntfs.md)<br/>                                           | Caching controllo in Transactional NTFS.<br/>                                                                                    |
| [Come usare NTFS transazionale](how-to-use-transactional-ntfs.md)<br/>                                         | Gestione degli handle di file transazionali in NTFS transazionale.<br/>                                                                   |
| [Concetti di base di TxF](txf-basic-concepts.md)<br/>                                                               | Vengono descritti i concetti relativi alla coerenza con read committed, all'isolamento read-committed e al blocco transazionale in NTFS transazionale.<br/> |
| [Considerazioni sulla programmazione per NTFS transazionale](programming-considerations-for-transacted-fileio-.md)<br/> | Vengono descritte diverse considerazioni sulla programmazione per NTFS transazionale.<br/>                                                      |
| [Considerazioni sulle prestazioni per NTFS transazionale](performance-considerations-for-transactional-ntfs.md)<br/> | Consigli le transazioni file system ottimali.<br/>                                                                     |



 

 


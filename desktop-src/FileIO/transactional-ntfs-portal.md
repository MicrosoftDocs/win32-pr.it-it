---
description: Transactional NTFS (TxF) consente di eseguire operazioni su file su un volume file system NTFS in una transazione.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: Transactional NTFS (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524925"
---
# <a name="transactional-ntfs-txf"></a>Transactional NTFS (TxF)

\[Microsoft consiglia vivamente agli sviluppatori di utilizzare metodi alternativi per soddisfare le esigenze dell'applicazione. Molti scenari in cui TxF è stato sviluppato possono essere realizzati attraverso tecniche più semplici e più facilmente disponibili. Inoltre, è possibile che TxF non sia disponibile nelle versioni future di Microsoft Windows. Per altre informazioni e per le alternative a TxF, vedere [alternative all'uso di Transactional NTFS](deprecation-of-txf.md).\]

## <a name="purpose"></a>Scopo

Transactional NTFS (TxF) consente di eseguire operazioni su file su un volume file system NTFS in una transazione. Le transazioni TxF aumentano l'affidabilità dell'applicazione proteggendo l'integrità dei dati tra errori e semplificando lo sviluppo di applicazioni riducendo notevolmente la quantità di codice di gestione degli errori.

TxF utilizza il Framework di transazione fornito da [gestione transazioni kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal) . In questo modo le operazioni di file TxF possono far parte di una transazione che interessa altre origini dati, ad esempio SQL Server e il registro di sistema transazionale (TxR).

## <a name="where-applicable"></a>Se applicabile

Un'applicazione può usare TxF per mantenere l'integrità dei dati su disco causati da condizioni di errore impreviste e risolvere gli scenari utente del file System simultanei isolando le modifiche da altri utenti durante le modifiche apportate.

## <a name="developer-audience"></a>Sviluppatori

Prima di utilizzare TxF, è necessario disporre di una conoscenza operativa delle transazioni utilizzando KTM o [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).

## <a name="run-time-requirements"></a>Requisiti di runtime

TxF è disponibile a partire da Windows Vista.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                    | Descrizione                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Informazioni](about-transactional-ntfs.md)<br/>         | Informazioni generali sul formato NTFS transazionale.<br/>                                                   |
| [Riferimento](transactional-ntfs-reference.md)<br/> | Documentazione per le funzioni, le strutture dei dati, le enumerazioni e altri elementi di programmazione.<br/> |



 

 


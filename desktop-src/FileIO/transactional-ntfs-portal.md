---
description: Ntfs transazionale (TxF) consente di eseguire operazioni su file in un volume file system NTFS in una transazione.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS transazionale (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5b44a35e4f83c1389d1fc2e6bc3de4f97f5ad203bbdee4750c2fcd26d87f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431911"
---
# <a name="transactional-ntfs-txf"></a>NTFS transazionale (TxF)

\[Microsoft consiglia vivamente agli sviluppatori di usare mezzi alternativi per soddisfare le esigenze dell'applicazione. Molti scenari per cui TxF è stato sviluppato possono essere ottenuti tramite tecniche più semplici e più facilmente disponibili. Inoltre, TxF potrebbe non essere disponibile nelle versioni future di Microsoft Windows. Per altre informazioni e alternative a TxF, vedere [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]

## <a name="purpose"></a>Scopo

Ntfs transazionale (TxF) consente di eseguire operazioni su file in un volume file system NTFS in una transazione. Le transazioni TxF aumentano l'affidabilità dell'applicazione proteggendo l'integrità dei dati tra gli errori e semplificando lo sviluppo delle applicazioni riducendo notevolmente la quantità di codice di gestione degli errori.

TxF usa il framework delle transazioni fornito da [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM). Ciò consente alle operazioni sui file TxF di far parte di una transazione che interessa altre origini dati, ad esempio SQL Server e Transacted Registry (TxR).

## <a name="where-applicable"></a>Se applicabile

Un'applicazione può usare TxF per mantenere l'integrità dei dati su disco causati da condizioni di errore impreviste e contribuire a risolvere scenari utente simultanei del file system isolando le modifiche da altri durante l'esecuzione delle modifiche.

## <a name="developer-audience"></a>Sviluppatori

Prima di usare TxF, è necessario avere una conoscenza funzionante delle transazioni usando KTM o [Distributed Transaction Coordinator (DTC).](/previous-versions/windows/desktop/ms684146(v=vs.85))

## <a name="run-time-requirements"></a>Requisiti di runtime

TxF è disponibile a partire da Windows Vista.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                    | Descrizione                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Informazioni](about-transactional-ntfs.md)<br/>         | Informazioni generali su NTFS transazionale.<br/>                                                   |
| [Riferimento](transactional-ntfs-reference.md)<br/> | Documentazione per funzioni, strutture di dati, enumerazioni e altri elementi di programmazione.<br/> |



 

 


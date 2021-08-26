---
description: Implementare Transactional NTFS (TxF) e Transactional Registry (TxR). TxF consente operazioni di file system transazione all'interno di NTFS. TxR consente operazioni del Registro di sistema transazione. Coordinare file system e le operazioni del Registro di sistema con una transazione.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Gestione transazioni kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c446931fff4f119217a5f6e5f1b7ae8cf351cf94966a9da5abc4e4d2e88d787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897531"
---
# <a name="kernel-transaction-manager"></a>Gestione transazioni kernel

## <a name="purpose"></a>Scopo

Kernel Transaction Manager (KTM) consente lo sviluppo di applicazioni che usano transazioni. Il motore di transazione stesso si trova all'interno del kernel, ma le transazioni possono essere sviluppate per transazioni in modalità kernel o utente e all'interno di un singolo host o tra host distribuiti.

KTM viene usato per implementare Transactional NTFS (TxF) e Transactional Registry (TxR). TxF consente operazioni di file system transazione all'interno dell'file system NTFS. TxR consente operazioni del Registro di sistema transazione. KTM consente alle applicazioni client di coordinare file system e le operazioni del Registro di sistema con una transazione.

Per sviluppare un'applicazione che coordina le transazioni con risorse diverse da TxF o TxR, è innanzitutto necessario sviluppare un servizio win32 in grado di riconoscere le transazioni, denominato anche gestore delle risorse.

Le applicazioni gestite e COM+ devono usare i gestori delle transazioni nativi.

## <a name="where-applicable"></a>Se applicabile

KTM può essere usato con applicazioni e resource manager ospitati in Windows Vista o Windows Server 2008.

## <a name="developer-audience"></a>Sviluppatori

L'API KTM è progettata per l'uso da parte dei programmatori C e C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

KTM è supportato a partire da Windows Vista.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                     | Descrizione                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Informazioni](about-ktm.md)<br/>         | Informazioni generali sulle transazioni e sulle funzionalità fornite da KTM.<br/>                           |
| [Riferimento](ktm-reference.md)<br/> | Documentazione per funzioni, strutture di dati, enumerazioni e altri elementi di programmazione di KTM.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[NTFS transazionale (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 


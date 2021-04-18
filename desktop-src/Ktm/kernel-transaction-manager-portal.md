---
description: Implementare il registro di sistema transazionale NTFS (TxF) e transazionale (TxR). TxF consente operazioni transazionali file system all'interno di NTFS. TxR consente operazioni del registro di sistema transazionali. Coordinare file system e le operazioni del registro di sistema con una transazione.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Gestione transazioni kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317139"
---
# <a name="kernel-transaction-manager"></a>Gestione transazioni kernel

## <a name="purpose"></a>Scopo

Gestione transazioni kernel consente lo sviluppo di applicazioni che utilizzano transazioni. Il motore di transazione stesso si trova all'interno del kernel, ma è possibile sviluppare transazioni per transazioni in modalità kernel o utente e all'interno di un singolo host o tra host distribuiti.

La KTM viene utilizzata per implementare il registro di sistema transazionale NTFS (TxF) e transazionale (TxR). TxF consente operazioni transazionali file system all'interno del file system NTFS. TxR consente operazioni del registro di sistema transazionali. KTM consente alle applicazioni client di coordinare file system e operazioni del registro di sistema con una transazione.

Per sviluppare un'applicazione che coordina le transazioni con risorse diverse da TxF o TxR, è necessario innanzitutto sviluppare un servizio in grado di riconoscere le transazioni Win32, detto anche Resource Manager.

Le applicazioni gestite e COM+ devono usare i relativi gestori transazioni nativi.

## <a name="where-applicable"></a>Se applicabile

È possibile utilizzare KTM con le applicazioni e i gestori di risorse ospitati in Windows Vista o Windows Server 2008.

## <a name="developer-audience"></a>Sviluppatori

L'API KTM è progettata per l'uso da parte dei programmatori C e C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

KTM è supportato a partire da Windows Vista.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                     | Descrizione                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Informazioni](about-ktm.md)<br/>         | Informazioni generali sulle transazioni e sulle funzionalità fornite da KTM.<br/>                           |
| [Riferimento](ktm-reference.md)<br/> | Documentazione per le funzioni, le strutture dei dati, le enumerazioni e altri elementi di programmazione di KTM.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[Transactional NTFS (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 


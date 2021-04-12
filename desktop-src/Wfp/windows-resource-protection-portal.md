---
description: La protezione delle risorse impedisce la sostituzione di file di sistema e cartelle e chiavi del registro di sistema essenziali per il sistema operativo. La modifica delle risorse protette può causare un errore di sistema o dell'applicazione.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Protezione risorse di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347216"
---
# <a name="windows-resource-protection"></a>Protezione risorse di Windows

## <a name="purpose"></a>Scopo

Protezione risorse di Windows (WRP) impedisce la sostituzione dei file di sistema essenziali, delle cartelle e delle chiavi del registro di sistema installate come parte del sistema operativo. È diventato disponibile a partire da Windows Server 2008 e Windows Vista. Le applicazioni non devono sovrascrivere queste risorse perché vengono usate dal sistema e da altre applicazioni. La protezione di queste risorse impedisce gli errori dell'applicazione e del sistema operativo. WRP è il nuovo nome per la protezione dei file di Windows (WFP). WRP protegge le chiavi del registro di sistema e le cartelle, nonché i file di sistema essenziali.

## <a name="where-applicable"></a>Se applicabile

Tutte le applicazioni basate su Windows e i relativi programmi di installazione eseguiti in Windows Server 2008 o Windows Vista e nei sistemi operativi successivi devono essere a conoscenza di WRP. Tutte le applicazioni basate su Windows in esecuzione su Microsoft Windows Server 2003 o Windows XP e i relativi programmi di installazione devono essere a conoscenza di Pam.

## <a name="developer-audience"></a>Sviluppatori

L'API WRP è progettata per l'uso da parte dei programmatori C/C++. L'API WRP ha due funzioni: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).

## <a name="run-time-requirements"></a>Requisiti di runtime

Le applicazioni che usano solo la funzione [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) richiedono windows Server 2008, Windows Vista, windows Server 2003 o Windows XP. Le applicazioni che usano la funzione [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) richiedono windows Server 2008 o Windows Vista.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [Informazioni su Protezione risorse di Windows](about-windows-file-protection.md)<br/>         | Informazioni generali su WRP.<br/>   |
| [Riferimento Protezione risorse di Windows](windows-file-protection-reference.md)<br/> | Documentazione di riferimento per WRP.<br/> |



 

 

 





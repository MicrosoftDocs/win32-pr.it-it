---
description: L'uso di Internet Explorer (LCIE) consente di migliorare l'affidabilità del browser separando i componenti e allentando l'interdipendenze.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Architettura (Windows 7 e Windows cookbook sulla qualità delle applicazioni di Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a635f686c804a6c81146f156a0b70869edf4405e8d7c86d1fab8cfad9b21c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134124"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Architettura (Windows 7 e Windows cookbook sulla qualità delle applicazioni di Server 2008 R2)

*L'Internet Explorer* (LCIE) consente di migliorare l'affidabilità del browser separando i componenti e allentando l'interdipendenze.

In particolare, LCIE tenta di isolare Windows Internet Explorer frame e le relative schede in processi separati. In Windows Internet Explorer 8, questo isolamento migliora le prestazioni e la scalabilità. Questa modifica dell'architettura potrebbe influire sulla compatibilità di estensioni e componenti aggiuntivi, inclusi i controlli ActiveX, gli oggetti BROWSER Helper Objects e i componenti della barra degli strumenti dell'interfaccia utente compilati usando tecniche di programmazione precedenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettare aggiornamenti che influiscono sulla compatibilità tra browser](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 




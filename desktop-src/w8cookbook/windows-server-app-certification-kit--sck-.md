---
title: Microsoft Platform Ready Test Tool
description: Microsoft Platform Ready Test Tool
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730727"
---
# <a name="microsoft-platform-ready-test-tool"></a>Microsoft Platform Ready Test Tool

## <a name="platform"></a>Piattaforma

 **Server** : windows Server 2012 \| Windows Server 2012 R2  

## <a name="description"></a>Descrizione

Lo strumento di test Microsoft Platform Ready (MPR) viene usato per la preparazione delle applicazioni per la piattaforma e per convalidare la conformità ai requisiti di certificazione per le applicazioni Windows Server 2012 e Windows Server 2012 R2.

Microsoft consiglia vivamente di incorporare lo strumento di test di MPR nei processi di compilazione e test del software, garantendo in tal modo la preparazione della piattaforma prima che le applicazioni vengano rilasciate sul mercato. Lo strumento di test di MPR è inoltre uno strumento consigliato per testare le applicazioni line-of-business e per valutare i prodotti server per la compatibilità della piattaforma prima di prendere decisioni di acquisto.

## <a name="requirements"></a>Requisiti

Lo strumento di test di MPR include test automatizzati per:

-   Windows Installer
-   Installazione e funzionalità primarie
-   Driver e sicurezza
-   Procedure consigliate

Il test automatico e l'invio di risultati per la maggior parte delle app Server dovrebbero richiedere almeno due ore; app più complesse possono richiedere circa 4 ore.

Tutti i driver devono passare separatamente i test di certificazione hardware Windows ed essere firmati da Microsoft per Windows Server 2012.

## <a name="usage"></a>Utilizzo

Per testare le app:

1.  Installare la versione più recente di Windows Server 2012 Configuration (GUI completa, interfaccia server minima o Server Core) in base alle esigenze dell'app.
2.  Esaminare i requisiti di certificazione.
3.  In un sistema pulito eseguire lo strumento di test di MPR in modalità interfaccia utente completa o in modalità riga di comando.
4.  Completare il processo di test guidato autonomamente.
5.  Esaminare i risultati e correggere l'app secondo le esigenze.
6.  Eseguire l'accesso e caricare i risultati nel portale di Microsoft Platform Ready per l'elenco nel catalogo di Windows Server e l'utilizzo del logo.

## <a name="resources"></a>Risorse

-   [Requisiti per il programma di certificazione delle app di Windows Server](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Microsoft Platform Ready (MPR) Test Tool](https://www.microsoft.com/download/details.aspx?id=37143)
-   [Programma di certificazione applicazioni Windows Server 2012](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [Commenti sul logo di Windows Server](mailto:WSLogoFB@microsoft.com)

 

 
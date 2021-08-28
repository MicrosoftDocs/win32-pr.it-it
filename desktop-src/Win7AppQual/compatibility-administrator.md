---
description: Compatibility Administrator
ms.assetid: 72a77e83-ab18-438c-af11-fa6d55bf0180
title: Compatibility Administrator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504378dd4998118e0189a40d978b5649a0bc0215e88ff660d7cdafa6edf7602c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098541"
---
# <a name="compatibility-administrator"></a>Compatibility Administrator

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client:** Windows 2000, Windows XP, Windows Vista, Windows 7  
**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="description"></a>Descrizione

Lo strumento Di amministrazione compatibilità, fornito da Application Compatibility Toolkit (ACT) consente di risolvere molti dei potenziali problemi di compatibilità delle applicazioni, prima di distribuire una nuova versione di Windows all'organizzazione, tramite:

-   Fornire singole correzioni di compatibilità, modalità di compatibilità e messaggi di AppHelp che è possibile usare per risolvere problemi di compatibilità specifici
-   Possibilità di creare correzioni di compatibilità, modalità di compatibilità, messaggi di AppHelp e database di compatibilità personalizzati
-   Fornire uno strumento di query che consente di cercare le correzioni installate nei computer locali

## <a name="usage"></a>Utilizzo

Il diagramma di flusso seguente illustra i passaggi necessari per usare Amministrazione compatibilità per creare le correzioni di compatibilità, le modalità di compatibilità e i messaggi di AppHelp.



| &nbsp;    | &nbsp;  |  &nbsp;   | &nbsp;  | &nbsp; | &nbsp;  |  &nbsp;  |
|--------------------------------------------|----------|--------------------------------------------------------------------------------------------|----------|-----------------------------------------------------|----------|-----------------------------------------------------------------------------|
| Creare un nuovo database di compatibilità (con estensione sdb) | **>** | Selezionare l'applicazione e quindi selezionare le correzioni di compatibilità da applicare all'applicazione | **>** | Testare l'applicazione con la nuova correzione di compatibilità | **>** | Salvare il database di compatibilità e quindi distribuire la correzione all'azienda |



 

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Compatibilità delle applicazioni Toolkit download](/windows-hardware/get-started/adk-install)
-   [Uso di Amministrazione compatibilità](/previous-versions/windows/it-pro/windows-7/cc749034(v=ws.10))
-   [Correzioni di compatibilità note, modalità di compatibilità e messaggi di AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [Test e mitigazione dei problemi tramite gli strumenti di sviluppo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))

 

 

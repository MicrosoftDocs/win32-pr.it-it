---
description: La preparazione delle risorse per un'applicazione MUI supporta sia i modelli PE Win32 che quelli non Win32.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Preparazione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317144"
---
# <a name="preparing-resources"></a>Preparazione delle risorse

La preparazione delle risorse per un'applicazione MUI supporta sia i modelli PE Win32 che quelli non Win32. Le risorse PE Win32 sono disponibili nei file basati su PE, ad esempio i file con estensione dll, exe o sys. Le risorse PE non Win32 sono fornite in un modulo personalizzato di propria scelta.

> [!Note]  
> Si consiglia vivamente di utilizzare le risorse PE Win32 per le applicazioni MUI Win32, in quanto queste risorse sono completamente supportate dalla tecnologia delle risorse MUI. È possibile individuare i file di risorse PE non Win32 chiamando la funzione [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) come descritto in [individuazione di risorse PE non Win32](locating-non-win32-pe-resources.md), ma l'applicazione deve fornire le proprie funzionalità per individuare e caricare le risorse necessarie.

 

Questa sezione contiene i seguenti argomenti:

-   [Creazione del file di risorse della lingua di base](creating-the-base-language-resource-file.md)
-   [Uso del reindirizzamento delle stringhe del registro di sistema](using-registry-string-redirection.md)
-   [Preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md)

 

 




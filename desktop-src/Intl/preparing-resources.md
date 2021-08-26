---
description: La preparazione delle risorse per un'applicazione MUI supporta sia i modelli PE Win32 che non Win32 PE.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Preparazione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef40453ca6db40bed1c07bad80f7e21cb7adaa7ea48ae8ee5ce2a2a5c657ba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040671"
---
# <a name="preparing-resources"></a>Preparazione delle risorse

La preparazione delle risorse per un'applicazione MUI supporta sia i modelli PE Win32 che non Win32 PE. Le risorse PE Win32 vengono fornite in file basati su PE, ad esempio .dll, .exe o .sys file. Le risorse PE non Win32 sono fornite in un modulo personalizzato a scelta.

> [!Note]  
> È consigliabile usare le risorse PE Win32 per le applicazioni MUI Win32, perché queste risorse sono completamente supportate dalla tecnologia delle risorse MUI. I file di risorse PE non Win32 possono essere individuati chiamando la funzione [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) come descritto in Individuazione di risorse [PE non Win32,](locating-non-win32-pe-resources.md)ma l'applicazione deve fornire la propria funzionalità per trovare e caricare le risorse necessarie.

 

Questa sezione contiene i seguenti argomenti:

-   [Creazione del file di risorse della lingua di base](creating-the-base-language-resource-file.md)
-   [Uso del reindirizzamento delle stringhe del Registro di sistema](using-registry-string-redirection.md)
-   [Preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md)

 

 




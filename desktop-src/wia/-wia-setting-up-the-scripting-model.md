---
description: Per utilizzare il modello di scripting Windows Image Acquisition (WIA), è necessario che il file Wiascr.dll installato e registrato nel computer.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Configurazione dell'ambiente di sviluppo del modello di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226141"
---
# <a name="setting-up-the-scripting-model-development-environment"></a>Configurazione dell'ambiente di sviluppo del modello di scripting

Per utilizzare il modello di scripting Windows Image Acquisition (WIA), è necessario che il file Wiascr.dll installato e registrato nel computer.

> [!Note]  
> Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA). Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Copiare questo file da WIA SDK nella directory *% windir%*/system32 (ad esempio, c: \\ Windows \\ System32). Nella riga di comando passare a questa directory e digitare **regsvr32 Wiascr.dll**.

Questa operazione immette le informazioni necessarie nel registro di sistema.

A questo punto è possibile usare il modello di scripting WIA.

 

 

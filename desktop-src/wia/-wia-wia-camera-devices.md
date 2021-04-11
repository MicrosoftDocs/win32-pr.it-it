---
description: WIA rappresenta un dispositivo della fotocamera come albero gerarchico di oggetti IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivi della fotocamera WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226137"
---
# <a name="wia-camera-devices"></a>Dispositivi della fotocamera WIA

WIA rappresenta un dispositivo della fotocamera come albero gerarchico di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . L'elemento radice, restituito da una chiamata al metodo gestione dispositivi Windows Image Acquisition (WIA) [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) , viene usato per ottenere e impostare le informazioni sul dispositivo, per controllare il dispositivo e per iniziare l'enumerazione degli elementi del dispositivo.

> [!Note]  
> WIA non supporta le fotocamere in Windows Vista o versioni successive. Per queste versioni di Windows, usare l'API Windows Portable Device (WPD) descritta in Windows Driver Development Kit (DDK) per acquisire immagini dalle fotocamere.

 

Il diagramma seguente illustra un'implementazione della fotocamera di esempio. L'elemento radice della fotocamera ha tre elementi figlio, due immagini e una cartella. La cartella contiene due elementi figlio, entrambe immagini.

![implementazione della fotocamera di esempio](images/wihierar.gif)

 

 




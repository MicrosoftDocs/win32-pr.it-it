---
description: WIA rappresenta un dispositivo fotocamera come albero gerarchico di oggetti IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivi fotocamera WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2023af90df6f868dfcace6f088bfe7ffeb6b549e0e20661231497f3fdf014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592726"
---
# <a name="wia-camera-devices"></a>Dispositivi fotocamera WIA

WIA rappresenta un dispositivo fotocamera come albero gerarchico di [**oggetti IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) L'elemento radice, restituito da una chiamata al metodo [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) di gestione dispositivi di Windows Image Acquisition (WIA), viene usato per ottenere e impostare le informazioni sul dispositivo, per controllare il dispositivo e per avviare l'enumerazione degli elementi del dispositivo.

> [!Note]  
> WIA non supporta le fotocamere in Windows Vista o versioni successive. Per queste versioni del Windows, usare l'API Windows Portable Device (WPD) descritta in Windows Driver Development Kit (DDK) per acquisire immagini dalle fotocamere.

 

Il diagramma seguente illustra un'implementazione della fotocamera di esempio. L'elemento radice della fotocamera ha tre elementi figlio, due immagini e una cartella. La cartella ha due elementi figlio, entrambe le immagini.

![implementazione di una fotocamera di esempio](images/wihierar.gif)

 

 




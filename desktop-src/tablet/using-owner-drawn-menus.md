---
description: Uso di menu disegnati dal proprietario per supportare la funzionalità di riconoscimento vocale per Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Uso Owner-Drawn menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14e63e3602e31edc506a6c9c070fa0bfcce670ec2248c73d68944a2f83a12f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842801"
---
# <a name="using-owner-drawn-menus"></a>Uso Owner-Drawn menu

Quando si usano menu disegnati dal proprietario, è necessario rendere disponibili i nomi dei menu per supportare la funzionalità di riconoscimento vocale. A questo scopo è possibile procedere in due modi:

-   Esporre il nome della voce di menu usando la struttura MSAAMENUINFO.
-   Consente di sostituire i menu grafici con menu di testo standard quando è attivo un supporto per l'accessibilità. Se la [**funzione SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) restituisce **TRUE** con il parametro *uiAction* impostato su SPI \_ GETSCREENREADER, usare i menu standard. L'applicazione deve controllare il messaggio WM SETTINGSCHANGE e rispondere tramite query sullo stato di questa opzione e regolando \_ la visualizzazione in modo appropriato. Ad esempio, Microsoft Visual Studio è possibile usare menu standard anziché i menu personalizzati visualizzati per impostazione predefinita.

 

 

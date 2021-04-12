---
title: Porting di funzioni di anti-aliasing
description: Porting di funzioni di anti-aliasing
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Porting di IRIS GL, anti-aliasing
- porting da IRIS GL, anti-aliasing
- porting in OpenGL da IRIS GL, anti-aliasing
- Porting OpenGL da IRIS GL, anti-aliasing
- anti-aliasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396827"
---
# <a name="porting-antialiasing-functions"></a>Porting di funzioni di anti-aliasing

In OpenGL la modalità subpixel è sempre attiva, di conseguenza la funzione di IRIS GL **subpixel**(**true**) non è necessaria e non ha un equivalente OpenGL. Negli argomenti seguenti vengono descritti gli aspetti della portabilità del codice di anti-aliasing IRIS GL.

-   [Porting del codice di fusione](porting-blending-code.md)
-   [Porting di funzioni di test AFunction](porting-afunction-test-functions.md)
-   [Uso di funzioni di anti-aliasing](using-antialiasing-functions.md)

 

 





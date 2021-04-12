---
title: Test di proprietà pixel
description: Il test di proprietà del pixel determina se il contesto OpenGL corrente è proprietario del pixel nel framebuffer corrispondente a un frammento specifico.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline di elaborazione OpenGL, test di proprietà pixel
- test di proprietà pixel OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330591"
---
# <a name="pixel-ownership-test"></a>Test di proprietà pixel

Il test di proprietà del pixel determina se il contesto OpenGL corrente è proprietario del pixel nel framebuffer corrispondente a un frammento specifico. In tal caso, il frammento procede al test successivo. In caso contrario, il sistema di Windows determina se il frammento viene eliminato o se verranno eseguite altre operazioni di frammento con tale frammento. Con questo test, il sistema finestra Controlla il comportamento quando, ad esempio, una finestra OpenGL viene nascosta.

 

 





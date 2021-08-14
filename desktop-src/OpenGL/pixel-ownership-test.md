---
title: Test di proprietà dei pixel
description: Il test di proprietà dei pixel determina se il contesto OpenGL corrente è proprietario del pixel nel framebuffer corrispondente a un particolare frammento.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline di elaborazione OpenGL, test di proprietà pixel
- Test di proprietà dei pixel OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cfefe133b3951fa70d51736f664ec5a7cb9942c4c05f892115dd222013f294
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936250"
---
# <a name="pixel-ownership-test"></a>Test di proprietà dei pixel

Il test di proprietà dei pixel determina se il contesto OpenGL corrente è proprietario del pixel nel framebuffer corrispondente a un particolare frammento. In tal caso, il frammento procede al test successivo. In caso contrario, il sistema di finestre determina se il frammento viene eliminato o se verranno eseguite altre operazioni sui frammenti con tale frammento. Con questo test, il sistema di finestre controlla il comportamento quando, ad esempio, una finestra OpenGL viene nascosta.

 

 





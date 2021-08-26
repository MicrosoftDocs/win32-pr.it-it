---
title: Commenti e suggerimenti
description: In modalità feedback, ogni primitiva da rasterizzarsi genera un blocco di valori che viene copiato nella matrice feedback.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modalità feedback, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5d307b9033a60a03b585cb4df6109293d3b9b0b276bde822ca595eb37fcd19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082451"
---
# <a name="feedback-mode"></a>Modalità feedback

In modalità feedback, ogni primitiva da rasterizzarsi genera un blocco di valori che viene copiato nella matrice feedback. Fornire questa matrice con [**glFeedbackBuffer,**](glfeedbackbuffer.md)che è necessario chiamare prima di impostare OpenGL in modalità feedback. Ogni blocco di valori inizia con un codice che indica il tipo primitivo, seguito da valori che descrivono i vertici della primitiva e i dati associati. Le voci vengono scritte anche per bitmap e rettangoli di pixel. Non è garantito che i valori siano scritti nella matrice di feedback fino a quando non si chiama [**glRenderMode**](glrendermode.md) per uscire dalla modalità feedback di OpenGL. È possibile usare [**glPassThrough**](glpassthrough.md) per fornire un marcatore restituito in modalità feedback come se fosse una primitiva.

 

 





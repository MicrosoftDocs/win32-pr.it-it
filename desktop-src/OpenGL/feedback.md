---
title: Commenti e suggerimenti
description: In modalità di feedback, ogni primitiva da rasterizzare genera un blocco di valori copiati nella matrice di commenti.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modalità feedback, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320837"
---
# <a name="feedback-mode"></a>Modalità feedback

In modalità di feedback, ogni primitiva da rasterizzare genera un blocco di valori copiati nella matrice di commenti. Specificare questa matrice con [**glFeedbackBuffer**](glfeedbackbuffer.md), che è necessario chiamare prima di inserire OpenGL in modalità feedback. Ogni blocco di valori inizia con un codice che indica il tipo primitivo, seguito da valori che descrivono i vertici della primitiva e i dati associati. Le voci vengono scritte anche per le bitmap e i rettangoli dei pixel. Non è garantito che i valori vengano scritti nella matrice di commenti fino a quando non si chiama [**glRenderMode**](glrendermode.md) per portare OpenGL fuori dalla modalità di feedback. È possibile utilizzare [**glPassThrough**](glpassthrough.md) per fornire un marcatore restituito in modalità feedback come se fosse una primitiva.

 

 





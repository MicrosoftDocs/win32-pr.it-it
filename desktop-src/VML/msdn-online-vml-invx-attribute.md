---
title: Attributo InvX di la
description: Attributo InvX di la
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728074"
---
# <a name="vml-invx-attribute"></a>Attributo InvX di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se la posizione x dell'handle è invertita. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[H](msdn-online-vml-h-element.md) (sottoelemento di [Handles](msdn-online-vml-handles-element.md))

**Sintassi Tag**

<v: *element* invx = " *Expression* " >

**Osservazioni:**

Se è **true**, la posizione x dell'handle viene invertita sottraendo il valore x dal valore x di **CoordOrigin** aggiunto al valore x di **CoordSize**. Il valore predefinito è **False**.

Questo attributo è l'equivalente di

coordorigin. x + coordsize. x-h. Position. x

*Attributo standard la*

 

 
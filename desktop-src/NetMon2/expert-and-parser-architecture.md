---
description: Nella figura seguente viene illustrata la relazione tra le applicazioni Expert e parser e altri componenti dell'architettura Network Monitor.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Architettura di esperti e parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128362"
---
# <a name="expert-and-parser-architecture"></a>Architettura di esperti e parser

Nella figura seguente viene illustrata la relazione tra le applicazioni [Expert](experts.md) e [parser](parsers.md) e altri componenti dell'architettura Network Monitor.

![relazione tra le applicazioni Expert e parser](images/nm-arch1.png)

Il traffico di rete viene raccolto come singoli frame dal driver NDIS. Il driver Network Monitor (Nmnt.sys) quindi instrada i frame a un provider di pacchetti di rete (NPP), che acquisisce i dati e li inserisce in uno o più file di acquisizione. NPP è una raccolta di interfacce COM utilizzate per acquisire i dati. In questo caso, l'interfaccia [**IDelaydC**](idelaydc.md) viene utilizzata per eseguire un'acquisizione ritardata.

> [!Note]  
> L'oggetto NPP viene usato per le acquisizioni ritardate e in tempo reale. Per le acquisizioni in tempo reale, viene usata l'interfaccia [**IRTC**](irtc.md) .

 

Quando i frame di rete vengono archiviati nel file di acquisizione e il file è accessibile, gli esperti e i parser possono utilizzare l'interfaccia utente di Network Monitor e le funzioni Network Monitor fornite in Nmapi.dll per analizzare i dati. I file di acquisizione non sono accessibili fino al completamento dell'acquisizione.

 

 




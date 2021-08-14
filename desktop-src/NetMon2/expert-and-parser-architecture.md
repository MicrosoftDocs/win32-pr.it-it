---
description: La figura seguente illustra la relazione tra applicazioni esperte e parser e altri componenti dell'Network Monitor architettura.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Architettura di esperti e parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261343005f0cb9fc7de5b7025f9ffe59f11515614ab43609c1b8da9f396e9f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795843"
---
# <a name="expert-and-parser-architecture"></a>Architettura di esperti e parser

La figura seguente illustra la relazione tra [applicazioni esperte](experts.md) [e parser](parsers.md) e altri componenti dell'Network Monitor architettura.

![relazione tra applicazioni esperte e parser](images/nm-arch1.png)

Il traffico di rete viene raccolto, come singoli frame, dal driver NDIS. Il Network Monitor driver (Nmnt.sys) instrada quindi i frame a un provider di pacchetti di rete (NPP), che acquisisce i dati e lo inserisce in uno o più file di acquisizione. NPP è una raccolta di interfacce COM usate per acquisire i dati. In questo caso, [**l'interfaccia IDelaydC**](idelaydc.md) viene usata per eseguire un'acquisizione ritardata.

> [!Note]  
> NPP viene usato per le acquisizioni in tempo reale e in ritardo. Per le acquisizioni in tempo reale, viene usata [**l'interfaccia IRTC.**](irtc.md)

 

Quando i frame di rete vengono archiviati nel file di acquisizione e il file è accessibile, esperti e parser possono usare l'interfaccia utente di Network Monitor e le funzioni Network Monitor fornite in Nmapi.dll per analizzare i dati. I file di acquisizione non sono accessibili fino al completamento dell'acquisizione.

 

 




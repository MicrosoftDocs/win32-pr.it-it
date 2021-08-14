---
description: L'impostazione della parte Etype o SAP del filtro di acquisizione è il primo passaggio del processo di creazione del filtro di acquisizione.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Impostazione del filtro Etype o SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac637594debf03ca9f82c79382ababc4c696d79d5351b2d0be0a3e5b4ffa8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363166"
---
# <a name="setting-the-etype-or-sap-filter"></a>Impostazione del filtro Etype o SAP

L'impostazione della parte Etype o SAP del filtro di acquisizione è il primo passaggio del processo di creazione del filtro di acquisizione.

Nell'esempio seguente il filtro di acquisizione è impostato per recuperare solo il traffico IPX:


```C++
BYTE Sap[]   = { 0x10, 0xE0 };
WORD Etype[] = { 0x8137 }; 

rc = SetNPPEtypeSapFilter(m_hBlob, 
     2,      //  nSaps,
     1,      //  nEtypes,
     &Sap,   //  LPBYTE lpSapTable,
     &Etype, //  LPWORD lpEtypeTable,
     0,      //  DWORD  FilterFlags,
     NULL
);
```



I valori SAP ed Etype sono in genere disponibili nelle RFC. Entrambi i valori SAP ed Etype possono essere in una matrice.

 

 




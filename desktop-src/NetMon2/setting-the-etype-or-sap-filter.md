---
description: L'impostazione della parte ETYPE o SAP del filtro di acquisizione è il primo passaggio del processo di creazione del filtro di acquisizione.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Impostazione del filtro ETYPE o SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee117e992968265be5a973f3f4017832ee6ca0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966764"
---
# <a name="setting-the-etype-or-sap-filter"></a>Impostazione del filtro ETYPE o SAP

L'impostazione della parte ETYPE o SAP del filtro di acquisizione è il primo passaggio del processo di creazione del filtro di acquisizione.

Nell'esempio seguente, il filtro di acquisizione è impostato in modo da recuperare solo il traffico IPX:


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



I valori SAP e ETYPE sono in genere disponibili in RFC. I valori SAP e ETYPE possono essere in una matrice.

 

 




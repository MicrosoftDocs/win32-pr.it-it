---
description: Rappresenta un pacchetto di quattro chiamate.
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PackedCallPkg
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 104e764725213f7030c90a0240641c7c9b063785
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965628"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span id="vspixengine.packedcallpkg"></span>Struttura PackedCallPkg

Rappresenta un pacchetto di quattro chiamate.

## <a name="syntax"></a>Sintassi


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a>Members

**pcp1**  
Prima chiamata nel pacchetto.

**pcp2**  
Seconda chiamata nel pacchetto.

**pcp3**  
Terza chiamata nel pacchetto.

**pcp4**  
Quarta chiamata nel pacchetto.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 




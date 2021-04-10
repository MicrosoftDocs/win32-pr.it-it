---
description: Ottiene la versione remota del motore.
MS-HAID: vspixengine.IPixEngine6\_GetRemotingVersion\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine6:: GetRemotingVersion'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 065FC3A7-ECFB-4551-B4B0-CA0E6B8676F8
api_name:
- IPixEngine6.GetRemotingVersion
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85230a71d9c0f2dd437ec25af3eb6c660f032586
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048988"
---
# <a name="span-idvspixengineipixengine6_getremotingversion_remotingversion_ptrspanipixengine6getremotingversion-method"></a><span id="vspixengine.ipixengine6_getremotingversion_remotingversion_ptr"></span>Metodo IPixEngine6:: GetRemotingVersion

Ottiene la versione remota del motore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRemotingVersion(
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a>Parametri

*pRemoteVersion*   
Versione remota del motore.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine6**](/windows/desktop/direct3dtools/ipixengine6)

 

 

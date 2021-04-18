---
description: Il metodo GetMaximumCursors Recupera il numero massimo di cursori supportati da un dispositivo tablet.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'Metodo ITablet3:: GetMaximumCursors'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313919"
---
# <a name="itablet3getmaximumcursors-method"></a>Metodo ITablet3:: GetMaximumCursors

Il metodo **GetMaximumCursors** Recupera il numero massimo di cursori supportati da un dispositivo tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMaximumCursors* 
</dt> <dd>

Numero massimo di input supportati dal dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK in caso di esito positivo; in caso contrario, restituisce un codice di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> </dl>

 

 





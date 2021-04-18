---
description: 'Versione utilizzabile del metodo IMFSourceResolver:: EndCreateObjectFromURL.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: RemoteEndCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308279"
---
# <a name="remoteendcreateobjectfromurl"></a>RemoteEndCreateObjectFromURL

Versione utilizzabile del metodo [**IMFSourceResolver:: EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) .

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a>Commenti

Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo. Il metodo non viene visualizzato in vtable per l'interfaccia. Se [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) viene chiamato tra i limiti del processo, la Media Foundation DLL di proxy/stub converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                                                    |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 





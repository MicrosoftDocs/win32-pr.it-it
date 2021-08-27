---
description: Versione remota del metodo IMFPMPHost::CreateObjectByCLSID.
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: RemoteCreateObjectByCLSID (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2274eb66c2dcd3452e6c3fbad1ab300ba705333a78e8eaa761eab70c54104ca0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061191"
---
# <a name="remotecreateobjectbyclsid"></a>RemoteCreateObjectByCLSID

Versione remota del metodo [**IMFPMPHost::CreateObjectByCLSID.**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid)

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a>Commenti

Le applicazioni non possono chiamare direttamente questo metodo e gli oggetti non implementano questo metodo. Il metodo non viene visualizzato nella tabella vtable per l'interfaccia . Se [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) viene chiamato oltre i limiti del processo, la DLL proxy/stub di Media Foundation converte la chiamata in una chiamata al metodo remoto e quindi la converte nuovamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[Sessione multimediale PMP](pmp-media-session.md)
</dt> <dt>

[Percorso del supporto protetto](protected-media-path.md)
</dt> </dl>

 

 





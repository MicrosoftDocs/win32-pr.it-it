---
title: Proprietà ResourceLocator.ResourceURI (WSManDisp.h)
description: Ottiene o imposta l'URI della risorsa in un oggetto ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Proprietà ResourceURI Windows Gestione remota
- Proprietà ResourceURI Windows gestione remota, oggetto ResourceLocator
- ResourceLocator object Windows Remote Management , ResourceURI property
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323240462dad32ba757897798b663b78b373ebb3ab3e60c3387dd7da8eef4c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642861"
---
# <a name="resourcelocatorresourceuri-property"></a>ResourceLocator.ResourceURI - proprietà

Ottiene o imposta [*l'URI della risorsa*](windows-remote-management-glossary.md) in [**un oggetto ResourceLocator.**](resourcelocator.md) È possibile fornire un [**oggetto ResourceLocator**](resourcelocator.md) anziché specificare un URI di risorsa nelle operazioni dell'oggetto [**Session,**](session.md) ad esempio [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate**](session-enumerate.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Valore proprietà

Stringa che identifica la risorsa. Quando si imposta l'URI della risorsa per [**un oggetto ResourceLocator,**](resourcelocator.md) l'URI deve contenere solo il percorso.

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di percorso corretto per [**ResourceURI.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri)

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

Il percorso seguente non funziona perché contiene una chiave per un'istanza specifica. Usare il [**metodo ResourceLocator.AddSelector**](resourcelocator-addselector.md) per specificare una particolare istanza.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**IWSManResourceLocator::ResourceURI è** il metodo C++ corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 






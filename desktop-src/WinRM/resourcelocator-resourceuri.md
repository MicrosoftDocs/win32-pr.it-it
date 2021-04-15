---
title: Proprietà ResourceLocator. ResourceURI (WSManDisp. h)
description: Ottiene o imposta l'URI della risorsa in un oggetto ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà ResourceURI
- Gestione remota Windows proprietà ResourceURI, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, proprietà ResourceURI
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
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477687"
---
# <a name="resourcelocatorresourceuri-property"></a>Proprietà ResourceLocator. ResourceURI

Ottiene o imposta l' [*URI della risorsa*](windows-remote-management-glossary.md) in un oggetto [**resourceLocator**](resourcelocator.md) . È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Valore proprietà

Stringa che identifica la risorsa. Quando si imposta l'URI della risorsa per un oggetto [**resourceLocator**](resourcelocator.md) , l'URI deve contenere solo il percorso.

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di un percorso corretto per [**resourceUri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

Il percorso seguente non funziona perché contiene una chiave per un'istanza specifica. Usare il metodo [**resourceLocator. AddSelector**](resourcelocator-addselector.md) per specificare una particolare istanza.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**IWSManResourceLocator:: ResourceURI** è il metodo C++ corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 






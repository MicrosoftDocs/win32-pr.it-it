---
title: Proprietà ResourceLocator.FragmentPath (WSManDisp.h)
description: Ottiene o imposta il percorso di un frammento di risorsa o di una proprietà quando ResourceLocator viene usato nelle operazioni dell'oggetto Session, ad esempio Session.Get, Session.Put o Session.Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Proprietà FragmentPath Windows Remote Management
- Proprietà FragmentPath Windows gestione remota , oggetto ResourceLocator
- Oggetto ResourceLocator Windows gestione remota, proprietà FragmentPath
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f756d669ba79ce034a9562d6cae5d58653bc60e042344306fb18aa37edfdc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121631"
---
# <a name="resourcelocatorfragmentpath-property"></a>ResourceLocator.FragmentPath - proprietà

Ottiene o imposta il percorso di un frammento di risorsa o di una proprietà quando [**ResourceLocator**](resourcelocator.md) viene usato [**nelle**](session.md) operazioni dell'oggetto Session, ad esempio [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md) [](windows-remote-management-glossary.md) [](windows-remote-management-glossary.md)

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Valore proprietà

Stringa che identifica il frammento o la proprietà della risorsa. Ad esempio, se la risorsa è un'unità disco e la proprietà richiesta è Manufacturer, la stringa può contenere `Diskdrive/Manufacturer` . Il testo del frammento fa distinzione tra maiuscole e minuscole. In questo caso, non è possibile usare `diskdrive/manufacturer` .

## <a name="remarks"></a>Commenti

**IWSManResourceLocator::FragmentPath** è la proprietà C++ corrispondente.

È possibile specificare un elemento di una proprietà di matrice specificando l'indice della matrice, come illustrato nell'esempio seguente. Tenere presente che l'indicizzazione delle matrici inizia con 1 anziché con 0.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Per ottenere l'intera matrice, specificare il nome della proprietà della matrice, come illustrato nell'esempio seguente.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



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

 

 






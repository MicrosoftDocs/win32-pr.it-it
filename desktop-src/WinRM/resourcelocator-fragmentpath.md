---
title: Proprietà ResourceLocator. FragmentPath (WSManDisp. h)
description: Ottiene o imposta il percorso di una proprietà o di un frammento di risorsa quando ResourceLocator viene utilizzato nelle operazioni dell'oggetto sessione, ad esempio Session. Get, Session. put o Session. enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà FragmentPath
- Gestione remota Windows proprietà FragmentPath, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, proprietà FragmentPath
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
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048403"
---
# <a name="resourcelocatorfragmentpath-property"></a>Proprietà ResourceLocator. FragmentPath

Ottiene o imposta il percorso di una proprietà o di un [*frammento*](windows-remote-management-glossary.md) di [*risorsa*](windows-remote-management-glossary.md) quando [**resourceLocator**](resourcelocator.md) viene utilizzato nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Valore proprietà

Stringa che identifica il frammento o la proprietà della risorsa. Ad esempio, se la risorsa è un'unità disco e la proprietà richiesta è Manufacturer, la stringa può contenere `Diskdrive/Manufacturer` . Il testo del frammento fa distinzione tra maiuscole e minuscole. In questo caso, non è possibile utilizzare `diskdrive/manufacturer` .

## <a name="remarks"></a>Commenti

**IWSManResourceLocator:: FragmentPath** è la proprietà C++ corrispondente.

È possibile specificare un elemento di una proprietà di matrice fornendo l'indice della matrice, come illustrato nell'esempio seguente. Tenere presente che l'indicizzazione della matrice inizia con 1 anziché con 0.


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 






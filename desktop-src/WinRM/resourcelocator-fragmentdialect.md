---
title: Proprietà ResourceLocator. FragmentDialect (WSManDisp. h)
description: Ottiene o imposta il dialetto del linguaggio per un sottolinguaggio di frammenti di risorse quando ResourceLocator viene utilizzato nelle operazioni di oggetti sessione come Session. Get, Session. put o Session. enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà FragmentDialect
- Gestione remota Windows proprietà FragmentDialect, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, proprietà FragmentDialect
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478784"
---
# <a name="resourcelocatorfragmentdialect-property"></a>Proprietà ResourceLocator. FragmentDialect

Ottiene o imposta il dialetto del linguaggio per un *sottolinguaggio* di [*frammenti*](windows-remote-management-glossary.md) di [*risorse*](windows-remote-management-glossary.md) quando [**resourceLocator**](resourcelocator.md) viene utilizzato nelle operazioni di oggetti [**sessione**](session.md) come [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md). Un frammento rappresenta una proprietà o una parte di una risorsa. È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) . Il dialetto indica il linguaggio XML che descrive il frammento al servizio che implementa l' [protocollo WS-Management](ws-management-protocol.md) e riceve la richiesta.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Valore proprietà

Stringa XML che identifica la lingua utilizzata nella proprietà [**FragmentPath**](resourcelocator-fragmentpath.md) . Per impostazione predefinita, la stringa di dialetto è la specifica XPath 1,0. Per altre informazioni, vedere [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Commenti

[**IWSManResourceLocator:: FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) è la proprietà C++ corrispondente.

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

 

 






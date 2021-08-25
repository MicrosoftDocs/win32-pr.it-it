---
title: Proprietà ResourceLocator.FragmentDialect (WSManDisp.h)
description: Ottiene o imposta il dialetto della lingua per un dialetto del frammento di risorsa quando ResourceLocator viene usato nelle operazioni dell'oggetto Session, ad esempio Session.Get, Session.Put o Session.Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Proprietà FragmentDialect Windows Remote Management
- Proprietà FragmentDialect Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Windows gestione remota, proprietà FragmentDialect
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
ms.openlocfilehash: b2ae7cbbd71b4ccad24ecaa17d0fd635761f661bcd6dc95ebc0345e9164adcd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997301"
---
# <a name="resourcelocatorfragmentdialect-property"></a>ResourceLocator.FragmentDialect - proprietà

Ottiene o imposta il dialetto della lingua per un [](windows-remote-management-glossary.md) [](windows-remote-management-glossary.md) *dialetto* del frammento di risorsa quando [**ResourceLocator**](resourcelocator.md) viene usato [**nelle**](session.md) operazioni dell'oggetto Session, ad esempio [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md) Un frammento rappresenta una proprietà o una parte di una risorsa. È possibile fornire un [**oggetto ResourceLocator**](resourcelocator.md) anziché specificare un URI di risorsa nelle [**operazioni dell'oggetto**](session.md) Session. Il dialetto indica quale linguaggio XML descrive il frammento per il servizio che implementa il [protocollo WS-Management](ws-management-protocol.md) e riceve la richiesta.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Valore proprietà

Stringa XML che identifica il linguaggio usato nella [**proprietà FragmentPath.**](resourcelocator-fragmentpath.md) Il valore predefinito della stringa di dialetto è la specifica XPath 1.0. Per altre informazioni, vedere [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Commenti

[**IWSManResourceLocator::FragmentDialect è**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) la proprietà C++ corrispondente.

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

 

 






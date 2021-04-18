---
title: parola chiave declare_guid
description: La \_ parola chiave Declare GUID indica a MIDL di creare una variabile GUID nel file di intestazione generato.
keywords:
- declare_guid parola chiave MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320440"
---
# <a name="declare_guid-keyword"></a>dichiarare \_ GUID (parola chiave)

La parola chiave **Declare \_ GUID** indica a MIDL di creare una variabile GUID nel file di intestazione generato.

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome variabile* 
</dt> <dd>

Specifica un nome di variabile per l'identificatore nel file di intestazione generato.

</dd> <dt>

*guid*
</dt> <dd>

Specifica il [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) che si applicherà al nome della variabile nel file di intestazione generato.

</dd> </dl>

## <a name="examples"></a>Esempio

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a>Commenti

L'utilizzo di `declare_guid` equivale all'utilizzo `cpp_quote` di per generare una chiamata della `EXTERN_GUID` macro.

L'esempio precedente restituisce l'output seguente:

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

L' `declare_guid` istruzione viene fornita come praticità. Ha il vantaggio di usare la stessa sintassi GUID dell' [ `uuid` attributo](uuid.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**cpp_quote**](cpp-quote.md)
</dt> <dt>

[**uuid (attributo)**](uuid.md)
</dt> <dt>

[**Struttura GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>

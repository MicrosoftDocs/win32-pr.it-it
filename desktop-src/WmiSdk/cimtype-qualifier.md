---
description: Il qualificatore CIMType contiene testo che descrive il tipo di una proprietà.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Qualificatore CIMType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 86fad829bf1b2391a9bc97d5c6281a67cadae7d03672e8a6eb8093b7ff6152b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131673"
---
# <a name="cimtype-qualifier"></a>Qualificatore CIMType

Il **qualificatore CIMType** contiene testo che descrive il tipo di una proprietà.

Questo testo può essere il tipo MOF, ad esempio "string" e "sint32" o il tipo CIM, ad esempio "CIM \_ STRING" e "CIM \_ SINT32". Esiste una corrispondenza uno-a-uno tra il qualificatore **CIMType** e il tipo della proprietà usata nel *parametro pvtType* del metodo [**IWbemClassObject::Get.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)

Le due eccezioni sono:

-   [*Fare riferimento alle*](gloss-r.md)proprietà , che hanno il tipo **CIM \_ REFERENCE**, che contiene il valore "REF:classname". Il valore classname descrive il tipo di classe della proprietà reference.
-   Proprietà dell'oggetto incorporato, che hanno il **tipo CIM \_ OBJECT.**

Si noti, tuttavia, che il qualificatore **CIMType** può e deve essere usato per digitare più esattamente una proprietà di riferimento. Ad esempio, se la proprietà fa sempre riferimento a istanze della [**classe \_ LogicalDisk Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) il qualificatore **CIMType** deve essere impostato su:


```mof
"ref:Win32_LogicalDisk"
```



Per impostazione predefinita, il **qualificatore CIMType** di una proprietà di riferimento ha il tipo **ref**.

Come per le proprietà di riferimento, il **qualificatore CIMType** deve essere usato per digitare una proprietà dell'oggetto incorporato più esattamente con la sintassi seguente:


```mof
"object:EmbedClass"
```



Poiché WMI consente più tipi di quelli che possono essere espressi dalle costanti standard con il prefisso VT, il qualificatore \_ **CIMType** consente di interpretare i valori del tipo. Il **qualificatore CIMType** viene aggiunto automaticamente. Per altre informazioni, vedere [Tipi di dati MOF](mof-data-types.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori WMI standard**](standard-wmi-qualifiers.md)
</dt> <dt>

[Qualificatori WMI](wmi-qualifiers.md)
</dt> <dt>

[Aggiunta di un qualificatore](adding-a-qualifier.md)
</dt> </dl>

 


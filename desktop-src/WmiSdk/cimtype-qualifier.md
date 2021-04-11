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
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131983"
---
# <a name="cimtype-qualifier"></a>Qualificatore CIMType

Il qualificatore **CimType** contiene testo che descrive il tipo di una proprietà.

Questo testo può essere il tipo MOF, ad esempio "String" e "sint32", oppure il tipo CIM, ad esempio "CIM \_ String" e "CIM \_ sint32". Esiste una corrispondenza uno-a-uno tra il qualificatore **CimType** e il tipo della proprietà utilizzata nel parametro *PvtType* del metodo [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .

Le due eccezioni sono:

-   [*Proprietà di riferimento*](gloss-r.md), che hanno il tipo **CIM \_ Reference**, che contiene il valore "Ref: NomeClasse". Il valore ClassName descrive il tipo di classe della proprietà Reference.
-   Proprietà dell'oggetto incorporato, che hanno il tipo di **\_ oggetto CIM** .

Si noti, tuttavia, che il qualificatore **CimType** può e deve essere usato per digitare più esattamente una proprietà di riferimento. Se, ad esempio, la proprietà si riferisce sempre a istanze della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , il relativo qualificatore **CimType** deve essere impostato su:


```mof
"ref:Win32_LogicalDisk"
```



Per impostazione predefinita, il qualificatore **CimType** di una proprietà Reference dispone del tipo **ref**.

Come per le proprietà di riferimento, il qualificatore **CimType** deve essere usato per digitare più esattamente una proprietà dell'oggetto incorporato con la sintassi seguente:


```mof
"object:EmbedClass"
```



Poiché WMI consente più tipi rispetto a quelli che possono essere espressi dalle costanti standard con il \_ prefisso VT, il qualificatore **CimType** può essere utile per interpretare i valori di tipo. Il qualificatore **CimType** viene aggiunto automaticamente. Per ulteriori informazioni, vedere [tipi di dati MOF](mof-data-types.md).

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

 


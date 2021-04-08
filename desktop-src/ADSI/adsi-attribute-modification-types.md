---
title: Tipi di modifica degli attributi ADSI (IADs. h)
description: Usato con il membro dwControlCode della struttura di informazioni di ADS \_ attr \_ per specificare il tipo di operazione da eseguire quando un attributo viene modificato con il metodo SetObjectAttributes di IDirectoryObject.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- tipi di modifica degli attributi ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048076"
---
# <a name="adsi-attribute-modification-types"></a>Tipi di modifica degli attributi ADSI

Le costanti seguenti vengono usate con il membro **dwControlCode** della struttura [**di \_ \_ informazioni di ADS attr**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) per specificare il tipo di operazione da eseguire quando un attributo viene modificato con il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Per ulteriori informazioni sull'utilizzo di questi valori, vedere [modifica degli attributi con ADSI](modifying-attributes-with-adsi.md).

<dl> <dt>

<span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**Clear degli annunci \_ attr \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Causa la rimozione di tutti i valori di attributo da un oggetto.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_aggiornamento attr \_ ADS**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Comporta l'aggiornamento dei valori di attributo specificati.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**\_accodamento degli annunci attr \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Consente di accodare i valori di attributo specificati ai valori degli attributi esistenti.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**eliminazione degli annunci \_ attr \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Determina la rimozione dei valori di attributo specificati da un oggetto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Queste costanti sono progettate per essere usate con la struttura [**di \_ \_ informazioni attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) nel metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Queste costanti non devono essere confuse con i membri dell' [**enumerazione \_ \_ \_ enum dell'operazione della proprietà ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , che devono essere usati con il metodo [**IADs::P UTEX**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_info attr \_ ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[Modifica degli attributi con ADSI](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 






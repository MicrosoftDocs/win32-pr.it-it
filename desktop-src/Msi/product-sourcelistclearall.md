---
description: Metodo SourceListClearAll. l'oggetto prodotto rimuove tutte le origini per il prodotto. È possibile specificare il tipo di origine da rimuovere.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Metodo Product. SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325883"
---
# <a name="productsourcelistclearall-method"></a>Metodo Product. SourceListClearAll

Metodo **SourceListClearAll** . l'oggetto [**prodotto**](product-object.md) rimuove tutte le origini per il prodotto. È possibile specificare il tipo di origine da rimuovere.

## <a name="syntax"></a>Sintassi


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo di origine da rimuovere: MSISOURCETYPE \_ media, MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





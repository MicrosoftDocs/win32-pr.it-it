---
description: Archivia una matrice di byte che rappresenta la licenza DRM associata al flusso di byte.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2718ba8a13d8d0c00114449f1141be77db0d3f83930d3b3de2171719c3bdf2d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113551"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>Proprietà MFNETSOURCE \_ DRMNET \_ LICENSE \_ REPRESENTATION

Archivia una matrice di byte che rappresenta la licenza DRM associata al flusso di byte.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Matrice di byte (**BLOB**)

VT \_ BLOB

**blob**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ DRMNET \_ LICENSE \_ REPRESENTATION** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Questa proprietà è di sola lettura. Per ottenere il valore della proprietà dal flusso di byte di rete, chiamare **IPropertyStore::GetValue** e passare la **struttura PROPERTYKEY** nel *parametro key.* Il **membro fmtid** di **PROPERTYKEY** deve essere impostato sul GUID della proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 





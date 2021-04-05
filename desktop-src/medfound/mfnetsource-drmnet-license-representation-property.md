---
description: Archivia una matrice di byte che rappresenta la licenza DRM associata al flusso di byte.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: Proprietà MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753127"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>\_Proprietà di \_ rappresentazione della licenza MFNETSOURCE DRMNET \_

Archivia una matrice di byte che rappresenta la licenza DRM associata al flusso di byte.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Matrice di byte (**BLOB**)

\_BLOB VT

**blob**



## <a name="remarks"></a>Commenti

La **rappresentazione di \_ \_ licenza \_ Constant MFNETSOURCE DRMNET** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Questa proprietà è di sola lettura. Per ottenere il valore della proprietà dal flusso di byte di rete, chiamare **IPropertyStore:: GetValue** e passare la struttura **PropertyKey** nel parametro *Key* . Il membro **fmtid** di **PropertyKey** deve essere impostato sul GUID della proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 





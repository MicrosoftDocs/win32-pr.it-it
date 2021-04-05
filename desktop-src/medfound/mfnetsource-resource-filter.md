---
description: Contiene un puntatore all'interfaccia di callback IMFNetResourceFilter per il flusso di byte HTTP Microsoft Media Foundation.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: Proprietà MFNETSOURCE_RESOURCE_FILTER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754258"
---
# <a name="mfnetsource_resource_filter-property"></a>\_Proprietà del \_ filtro risorse MFNETSOURCE

Contiene un puntatore all'interfaccia di callback [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) per il flusso di byte http Microsoft Media Foundation.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**IUnknown \** _

VT \_ sconosciuto

_ *punkVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation. Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 

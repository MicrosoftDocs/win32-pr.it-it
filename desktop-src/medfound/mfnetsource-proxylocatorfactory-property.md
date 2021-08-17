---
description: Contiene un puntatore all'interfaccia IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: MFNETSOURCE_PROXYLOCATORFACTORY proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc06f58fc11e4d0dcff95274170a76b25160b584231bd2c9e39ed1949b1363e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954741"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a>Proprietà MFNETSOURCE \_ PROXYLOCATORFACTORY

Contiene un puntatore [**all'interfaccia IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Puntatore IUnknown**

VT \_ UNKNOWN

**punkVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYLOCATORFACTORY** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per fornire un localizzatore proxy personalizzato per l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

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
</dt> <dt>

[Supporto proxy per le origini di rete](proxy-support-for-network-sources.md)
</dt> </dl>

 

 





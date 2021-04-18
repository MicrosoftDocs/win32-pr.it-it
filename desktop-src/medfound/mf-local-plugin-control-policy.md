---
description: Specifica i criteri di controllo di un plug-in locale.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: Attributo MF_LOCAL_PLUGIN_CONTROL_POLICY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319608"
---
# <a name="mf_local_plugin_control_policy-attribute"></a>\_Attributo dei \_ criteri di controllo del plug-in locale MF \_ \_

Specifica i criteri di controllo di un plug-in locale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Impostare questo attributo su uno dei valori [**dei \_ \_ \_ criteri di controllo del plug**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) -in MF.

Questo attributo consente all'app di specificare un criterio locale più restrittivo rispetto ai criteri a livello di processo configurati da [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 





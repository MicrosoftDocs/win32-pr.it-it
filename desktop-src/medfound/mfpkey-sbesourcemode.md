---
description: Imposta la configurazione del flusso per l'origine multimediale WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c6b4fc0b248000f0540fd47fd7bbf8bba907994d1351144521bf162d330340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973370"
---
# <a name="mfpkey_sbesourcemode-property"></a>MFPKEY \_ SBESourceMode - proprietà

Imposta la configurazione del flusso per l'origine multimediale WTV.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**INT**

VT \_ INT

**intVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare l'origine multimediale WTV. Per impostare la proprietà, passare un [**puntatore IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

L'origine multimediale WTV legge Windows file di Show TV registrato (con estensione wtv e ms-drv).

Questa proprietà deve avere uno dei valori seguenti.

-   1: eseguire il mapping dei flussi audio disponibili a un singolo output, in base al sistema locale. Questa modalità è appropriata per la riproduzione. (impostazione predefinita).
-   2. Vengono selezionati tutti i flussi audio e i flussi secondari, ad esempio i flussi di dati e i sottotitoli. Questa modalità è appropriata per la modifica o la transcoding.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 

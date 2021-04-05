---
description: Imposta la configurazione di flusso per l'origine del supporto WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: Proprietà MFPKEY_SBESourceMode (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967164"
---
# <a name="mfpkey_sbesourcemode-property"></a>\_Proprietà SBESourceMode di MFPKEY

Imposta la configurazione di flusso per l'origine del supporto WTV.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**INT**

\_int VT

**intVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare l'origine del supporto WTV. Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

L'origine multimediale WTV legge i file di Windows registrato TV (con estensione wtv e MS-DRV).

Questa proprietà deve avere uno dei valori seguenti.

-   1: esegue il mapping dei flussi audio disponibili a un singolo output, in base al sistema locale. Questa modalità è appropriata per la riproduzione. (impostazione predefinita).
-   2. Vengono selezionati tutti i flussi audio e i sottoflussi, ad esempio didascalia e flussi di dati. Questa modalità è appropriata per la remuxing o la transcodifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 

---
description: Abilita la modalità di download privato nell'origine di rete.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: MFNETSOURCE_ENABLE_PRIVATEMODE proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e2ff972aa42753bb92be33fd6bf893d0578f28bf0ad29889a1b5986ba1a77c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113541"
---
# <a name="mfnetsource_enable_privatemode-property"></a>MFNETSOURCE \_ ENABLE \_ PRIVATEMODE - proprietà

Abilita la modalità di download privato nell'origine di rete.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Bool**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

Se questa proprietà è **TRUE,** la cache viene cancellata al termine della sessione.

La **costante \_ CLIENTGUID di MFNETSOURCE** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 





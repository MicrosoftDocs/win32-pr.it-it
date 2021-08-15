---
description: Specifica se il decodificatore deve eseguire la Lt-Rt ripiega.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76d086fd0f57262d249784fcabc5a98e8a18668cf0697618f3fbbe5528a2cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713811"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>Proprietà MFPKEY \_ WMADEC \_ LTRTOUTPUT

Specifica se il decodificatore deve eseguire la Lt-Rt ripiega.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**VT \_ BOOL**

## <a name="default-value"></a>Valore predefinito

**VARIANT \_ FALSE**

## <a name="remarks"></a>Commenti

Se il valore di questa proprietà è VARIANT FALSE e l'output è stereo, il \_ decodificatore audio usa una semplice ripiega del canale. Se il valore di questa proprietà è VARIANT TRUE, il decodificatore audio esegue una Lt-Rt (a matrice) ripiegata in stereo e quindi qualsiasi decodificatore Dolby Surround può essere usato per decodificare il surround a \_ matrice. Ad esempio, il decodificatore audio può Lt-Rt in basso sul contenuto 5.1 o 7.1.

Questa proprietà è supportata solo quando il decodificatore funge da oggetto multimediale DirectX (DMO). Non è supportato alcun tipo di fold down quando il decodificatore funge da Media Foundation Transform (MFT).

In Windows Vista, se si ottiene **un'interfaccia IPropertyStore** in un decodificatore audio, il decodificatore funge da MFT. Di conseguenza, questa proprietà non può essere usata Windows Vista. Per informazioni su quando un decodificatore funge da DMO o MFT, vedere le singole pagine di riferimento del codec in [Oggetti codec](codecobjects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 

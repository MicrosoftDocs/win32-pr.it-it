---
description: Specifica se il decodificatore deve eseguire Lt-Rt riduzioni.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: Proprietà MFPKEY_WMADEC_LTRTOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130542"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>MFPKEY \_ WMADEC- \_ Proprietà LTRTOUTPUT

Specifica se il decodificatore deve eseguire Lt-Rt riduzioni.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANTE \_ false**

## <a name="remarks"></a>Commenti

Se questa proprietà presenta un valore VARIANT \_ false e l'output è stereo, il decodificatore audio utilizza una semplice riduzione del canale. Se questa proprietà ha un valore VARIANT \_ true, il decodificatore audio esegue Lt-Rt (matrici) ripiegare verso il basso fino a stereo e quindi qualsiasi decodificatore Dolby surround può essere usato per decodificare il racchiuso in matrici. Ad esempio, il decodificatore audio potrebbe eseguire Lt-Rt riduzione del contenuto 5,1 o 7,1.

Questa proprietà è supportata solo quando il decodificatore funge da oggetto DMO (DirectX Media Object). Se il decodificatore funge da Media Foundation trasformazione (MFT), non è supportata alcuna riduzione di alcun tipo.

In Windows Vista, se si ottiene un'interfaccia **IPropertyStore** su un decoder audio, il decodificatore funge da MFT. Di conseguenza, questa proprietà non può essere utilizzata in Windows Vista. Per informazioni su quando un decodificatore funge da DMO o da un MFT, vedere le pagine di riferimento del singolo codec in [oggetti codec](codecobjects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 

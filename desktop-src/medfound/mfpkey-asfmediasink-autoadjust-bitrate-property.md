---
description: Specifica se il sink multimediale ASF regola automaticamente la velocità in bit.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: Proprietà MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320752"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a>\_ \_ Proprietà velocità in bit regolazione automatica ASFMEDIASINK MFPKEY \_

Specifica se il sink multimediale ASF regola automaticamente la velocità in bit.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**\_bool Variant**

\_bool VT

**boolVal**



## <a name="remarks"></a>Commenti

Se il valore di questa proprietà è VARIANT \_ true, il sink multimediale ASF regola automaticamente la velocità in bit del contenuto ASF in risposta alle caratteristiche dei flussi sottoposto a multiplexing.

Questa proprietà influisce sul comportamento del sink multimediale ASF quando un flusso causa un overflow dei parametri "leaky bucket" del sink:



| valore              | Comportamento                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ true**  | Il sink multimediale ASF regola automaticamente la velocità in bit del contenuto ASF in risposta alle caratteristiche dei flussi sottoposte a multiplexing. |
| **VARIANTE \_ false** | Il sink multimediale ASF usa il valore della velocità in bit del flusso fornito dall'applicazione.                                                                |



 

Il valore predefinito è **Variant \_ false**.

Impostare questa proprietà quando si configura il sink del supporto ASF. L'utilizzo dipende dalla funzione chiamata per creare il sink multimediale ASF:

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): esegue una query sul puntatore [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperato per l'interfaccia **IPropertyStore** .

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sul puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) specificato nel parametro *pContentInfo* .

Se si imposta questa proprietà su VARIANT \_ true, il sink multimediale ASF imposterà il flag di **velocità in bit di MFASF \_ multiplexer \_ AutoAdjust \_** in ASF Multiplexer. Vedere [**IMFASFMultiplexer:: Flags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).

Per ulteriori informazioni sul concetto di bucket con perdite, vedere l'argomento relativo al modello di buffer di bucket a perdita nella documentazione di Windows Media Format SDK.

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

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 





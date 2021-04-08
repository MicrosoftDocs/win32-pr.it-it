---
description: Archivia l'ora (in unità 100-nanosecondi) in corrispondenza della quale deve iniziare la presentazione, relativa all'inizio dell'origine del supporto.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: Attributo MF_PD_PLAYBACK_BOUNDARY_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058252"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a>\_ \_ \_ Attributo tempo limite riproduzione MF PD \_

Archivia l'ora (in unità 100-nanosecondi) in corrispondenza della quale deve iniziare la presentazione, relativa all'inizio dell'origine del supporto.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Commenti

L' \_ \_ \_ attributo tempo limite riproduzione MF PD \_ è facoltativo per le origini multimediali in una playlist. Questo valore indica l'ora di inizio effettiva della presentazione. Si consideri una playlist che include origini multimediali *Element1*, *element2* e *Element3* in una sequenza. 15 secondi dopo l'avvio della riproduzione di *Element1* , si verifica una modifica dinamica del flusso. Il nuovo flusso deve iniziare a riprodurre 15 secondi nella presentazione. Tuttavia, il fotogramma chiave più vicino al tempo di presentazione di 15 secondi è a 12 secondi per il nuovo flusso. Per avviare la nuova presentazione a 15 secondi, è necessario un contrassegno, in modo che gli esempi decodificati vengano eliminati da 12 secondi a 15 secondi.

Prima della transizione, l'evento [MENewPresentation](menewpresentation.md) viene generato dall'origine supporto. Viene restituito il descrittore di presentazione che contiene l'attributo dell' [ID dell'elemento di \_ \_ riproduzione \_ \_ MF PD](mf-pd-playback-element-id.md) per *Element1*. Contiene inoltre l' \_ \_ attributo di tempo limite riproduzione MF PD \_ \_ impostato su 15 secondi per indicare l'ora in cui si è verificata la transizione. L'origine multimediale esegue il contrassegno dopo 15 secondi dopo la decodifica, impedendo la visualizzazione dei frame da 12 a 15 secondi.

Questo valore influisce solo su Markin Time e non influisce sul modo in cui la sessione multimediale regola i timestamp. Questo attributo viene ignorato a meno che l'origine del supporto non indichi tramite l'attributo [ \_ ID dell'elemento di \_ riproduzione \_ \_ MF PD](mf-pd-playback-element-id.md) che questa presentazione è lo stesso elemento di riproduzione del precedente.

L' \_ attributo del \_ tempo limite per la riproduzione MF PD \_ \_ è simile a quello dell'attributo [MEDIASTART di MF \_ TOPONODE \_ ](mf-toponode-mediastart-attribute.md) impostato nel nodo della topologia. Per le applicazioni in esecuzione in Windows Vista, le origini multimediali che implementano [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devono usare **MF \_ TOPONODE \_ MEDIASTART** anziché l' \_ \_ ora limite di riproduzione MF PD \_ \_ .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





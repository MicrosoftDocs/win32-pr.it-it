---
description: Rappresenta un report di indirizzo civico.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: Oggetto LocationDisp.DispCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5646bd6df1a2523faf481bc867acc67dbd0a647b4cdf3f033d7327a66174d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129981"
---
# <a name="locationdispdispcivicaddressreport-object"></a>Oggetto LocationDisp.DispCivicAddressReport

\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Per accedere alla posizione da un'applicazione desktop, usare il [**Windows. API Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Rappresenta un report di indirizzo civico.

## <a name="members"></a>Membri

**L'oggetto LocationDisp.DispCivicAddressReport** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto LocationDisp.DispCivicAddressReport** ha queste proprietà.



| Proprietà                                                                              | Tipo di accesso          | Descrizione                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Sola lettura<br/> | Prima riga di un indirizzo civico.<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Sola lettura<br/> | Seconda riga di un indirizzo stradale.<br/>             |
| [**City**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Sola lettura<br/> | Nome della città.<br/>                                   |
| [**CountryRegion**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Sola lettura<br/> | Nome del paese o dell'area geografica.<br/>                      |
| [**DetailLevel**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Sola lettura<br/> | Livello di dettaglio per il report.<br/>                 |
| [**Postalcode**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Sola lettura<br/> | Codice postale.<br/>                                 |
| [**Stateprovince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Sola lettura<br/> | Nome dello stato o della provincia.<br/>                      |
| [**Timestamp**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Sola lettura<br/> | Data e ora di generazione del report.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile recuperare questo oggetto tramite la [**proprietà CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) di un [**oggetto CivicAddressReportFactory.**](locationdisp-civicaddressreportfactory.md) È possibile ricevere questo oggetto tramite [**l'evento NewCivicAddressReport.**](newcivicaddressreport.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                  |



 


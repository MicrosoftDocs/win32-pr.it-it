---
title: Tipi di dati IMAPI (Imapi2.h)
description: Le specifiche per i supporti ottici e i dispositivi associati definiscono i valori di intervallo per elementi quali la descrizione della struttura del DVD, la descrizione delle informazioni sul disco e le dimensioni della pagina delle funzionalità.
ms.assetid: 8797a8d0-5ce5-4b16-9d41-c22fa0d67dcf
keywords:
- ULONG_IMAPI2_DVD_STRUCTURE
- ULONG_IMAPI2_ADAPTER_DESCRIPTOR
- ULONG_IMAPI2_DEVICE_DESCRIPTOR
- ULONG_IMAPI2_DISC_INFORMATION
- ULONG_IMAPI2_TRACK_INFORMATION
- ULONG_IMAPI2_FEATURE_PAGE
- ULONG_IMAPI2_MODE_PAGE
- ULONG_IMAPI2_ALL_FEATURE_PAGES
- ULONG_IMAPI2_ALL_PROFILES
- ULONG_IMAPI2_ALL_MODE_PAGES
- ULONG_IMAPI2_NONZERO
- ULONG_IMAPI2_NOT_NEGATIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f003c2e03ff3d21623111d3d43a83cddf43e31c64557cfce18b5a401cdcd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612011"
---
# <a name="imapi-data-types"></a>Tipi di dati IMAPI

Le specifiche per i supporti ottici e i dispositivi associati definiscono i valori di intervallo per elementi quali la descrizione della struttura del DVD, la descrizione delle informazioni sul disco e le dimensioni della pagina delle funzionalità. IMAPI definisce i tipi ULONG (Unsigned Long integer) seguenti che applicano limiti di valori di intervallo. Questi tipi vengono definiti esclusivamente per la convalida IDL ottimale dei parametri e come supporto della documentazione per i chiamanti relativamente ai limiti massimi per determinate operazioni di trasferimento dei dati disponibili.


```C++
typedef ULONG ULONG_IMAPI2_DVD_STRUCTURE;
typedef ULONG ULONG_IMAPI2_ADAPTER_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DEVICE_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DISC_INFORMATION;
typedef ULONG ULONG_IMAPI2_TRACK_INFORMATION;
typedef ULONG ULONG_IMAPI2_FEATURE_PAGE;
typedef ULONG ULONG_IMAPI2_MODE_PAGE;
typedef ULONG ULONG_IMAPI2_ALL_FEATURE_PAGES;
typedef ULONG ULONG_IMAPI2_ALL_PROFILES;
typedef ULONG ULONG_IMAPI2_ALL_MODE_PAGES;
typedef ULONG ULONG_IMAPI2_NONZERO;
typedef ULONG ULONG_IMAPI2_NOT_NEGATIVE;
```





| Tipo di dati                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**STRUTTURA DEI \_ DVD IMAPI2 ULONG \_ \_**                | Intervallo: 0,65535 (0,0x0000FFFF)<br/> La struttura del DVD è limitata a 64 KB a causa di un campo di allocazione a due byte.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**DESCRITTORE \_ DELL'ADAPTER IMAPI2 ULONG \_ \_** | Intervallo: 0,268435455 (0,0x0FFFFFFF)<br/> Le dimensioni del descrittore dell'adapter non sono implicitamente limitate.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**DESCRITTORE \_ DI DISPOSITIVO IMAPI2 ULONG \_ \_**    | Intervallo: 0,268435455 (0,0x0FFFFFFF)<br/> Le dimensioni del descrittore di dispositivo non sono implicitamente limitate.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**INFORMAZIONI SUL \_ DISCO IMAPI2 ULONG \_ \_**       | Intervallo: 0,65538 (0,0x00010002)<br/> Le informazioni sul disco sono limitate a 64 KB più 2 byte per il campo delle dimensioni.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**INFORMAZIONI SULLA TRACCIA \_ IMAPI2 ULONG \_ \_**    | Intervallo: 0,65538 (0,0x00010002)<br/> Le informazioni di traccia sono limitate a 64 KB più 2 byte per il campo delle dimensioni.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**PAGINA DELLE \_ FUNZIONALITÀ IMAPI2 \_ DI ULONG \_**                   | Intervallo: 0.256 (0,0x00000100)<br/> Una singola pagina di funzionalità è limitata a 256 byte.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**PAGINA ULONG \_ IMAPI2 MODE (MODALITÀ IMAPI2 \_ ULONG) \_**                            | Intervallo: 0.257 (0,0x00000101)<br/> Una singola pagina in modalità è limitata a 257 byte.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ IMAPI2 \_ TUTTE LE PAGINE DELLE \_ \_ FUNZIONALITÀ**   | Intervallo: 0,65536 (0,0x00010000)<br/> Il numero di funzionalità è limitato a un campo a due byte.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ IMAPI2 \_ TUTTI I \_ PROFILI**                   | Intervallo: 0,63 (0,0x0000003F)<br/> Il numero di profili per un dispositivo è il numero di profili che rientrano in una singola funzionalità. Ogni profilo occupa quattro byte. Una singola funzionalità può contenere 252 byte di dati aggiuntivi, sufficienti per archiviare un massimo di 63 profili.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG \_ IMAPI2 \_ ALL \_ MODE \_ PAGES**            | Intervallo: 0,32763 (0,0x00007FFB)<br/> Numero di pagine della modalità per un dispositivo. Il conteggio, tramite MODE \_ SENSE10, è limitato a un campo a due byte.<br/> L'intestazione del parametro mode è di 8 byte. Ogni pagina è di almeno due byte. Il numero massimo di pagine in modalità è 32763: (65535 - 8)/2 arrotondato per esere arrotondato per e per intero.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ DIVERSO DA ZERO**                                   | Intervallo: 1,2147483647 (1,0x7FFFFFFF)<br/> Valore generico diverso da zero che può essere utilizzato per verificare che un valore sia diverso da zero.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ NON \_ NEGATIVO**                   | Intervallo: 0, 2147483647 (0,0x7FFFFFFF)<br/> Intero a 32 bit con valore non negativo.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Imapi2.h</dt> </dl> |



 

 






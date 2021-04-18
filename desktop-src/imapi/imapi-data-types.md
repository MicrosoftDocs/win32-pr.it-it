---
title: Tipi di dati IMAPi (imapi2. h)
description: Le specifiche per i supporti ottici e i dispositivi associati definiscono i valori di intervallo per elementi quali la descrizione della struttura del DVD, la descrizione delle informazioni del disco e le dimensioni della pagina della funzionalità.
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
ms.openlocfilehash: 7793bab123e2939bdc2f5a68bb705d7468da5666
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302390"
---
# <a name="imapi-data-types"></a>Tipi di dati IMAPi

Le specifiche per i supporti ottici e i dispositivi associati definiscono i valori di intervallo per elementi quali la descrizione della struttura del DVD, la descrizione delle informazioni del disco e le dimensioni della pagina della funzionalità. IMAPi definisce i seguenti tipi unsigned long integer (ULONG) che applicano i limiti dei valori di intervallo. Questi tipi sono definiti esclusivamente per la convalida IDL ottimale dei parametri e come supporto per la documentazione per i chiamanti relativi ai limiti superiori per determinate operazioni di trasferimento dei dati disponibili.


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
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**\_ \_ Struttura DVD ULONG \_ imapi2**                | Intervallo: 0, 65535 (0, 0x0000FFFF)<br/> La struttura del DVD è limitata a 64KB a causa di un campo di allocazione a 2 byte.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**\_Descrittore imapi2 dell' \_ Adapter ULONG \_** | Intervallo: 0, 268435455 (0, 0x0FFFFFFF)<br/> Le dimensioni del descrittore di adapter non sono implicitamente limitate.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**Descrittore di dispositivo ULONG \_ imapi2 \_ \_**    | Intervallo: 0, 268435455 (0, 0x0FFFFFFF)<br/> Le dimensioni del descrittore del dispositivo non sono implicitamente limitate.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**\_Informazioni del \_ disco \_ imapi2 ULONG**       | Intervallo: 0, 65538 (0, 0x00010002)<br/> Le informazioni sui dischi sono limitate a 64KB più 2 byte per il campo dimensione.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**\_Informazioni di \_ rilevamento \_ imapi2 ULONG**    | Intervallo: 0, 65538 (0, 0x00010002)<br/> Le informazioni di rilevamento sono limitate a 64KB più 2 byte per il campo dimensioni.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**\_Pagina della \_ funzionalità ULONG imapi2 \_**                   | Intervallo: 0256 (0, 0x00000100)<br/> Una singola pagina di funzionalità è limitata a 256 byte.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**\_ \_ Pagina modalità imapi2 \_ ULONG**                            | Intervallo: 0257 (0, 0x00000101)<br/> Una singola pagina modalità è limitata a 257 byte.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**\_Pagine di \_ tutte le \_ funzionalità \_ di imapi2 ULONG**   | Intervallo: 0, 65536 (0, 0x00010000)<br/> Il numero di funzionalità è limitato a un campo a 2 byte.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ imapi2 \_ tutti i \_ profili**                   | Intervallo: 0, 63 (0, 0x0000003F)<br/> Il numero di profili per un dispositivo è il numero di profili che rientrano in una singola funzionalità. Ogni profilo occupa quattro byte. Una singola funzionalità può contenere 252 byte aggiuntivi di dati, sufficiente per archiviare un massimo di 63 profili.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**\_Pagine di imapi2 di \_ tutti i \_ modi \_ ULONG**            | Intervallo: 0, 32763 (0, 0x00007FFB)<br/> Conteggio delle pagine della modalità per un dispositivo. Il conteggio, tramite la modalità \_ SENSE10, è limitato a un campo a 2 byte.<br/> L'intestazione del parametro mode è 8 byte. Ogni pagina è almeno di due byte. Il numero massimo di pagine in modalità è 32763: (65535-8)/2 arrotondato per difetto.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**\_Imapi2 ULONG \_ diverso da zero**                                   | Intervallo: 1, 2147483647 (1, 0x7FFFFFFF)<br/> Valore generico diverso da zero che può essere utilizzato per verificare che un valore non sia zero.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**\_Imapi2 ULONG \_ non \_ negativo**                   | Intervallo: 0, 2147483647 (0, 0x7FFFFFFF)<br/> Intero a 32 bit con valore non negativo.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Imapi2. h</dt> </dl> |



 

 






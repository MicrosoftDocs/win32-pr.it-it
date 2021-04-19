---
description: L' \_ enumerazione del set di caratteri BLOB \_ indica il set di caratteri usato dal BLOB di conferenza corrente.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Enumerazione BLOB_CHARACTER_SET (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329092"
---
# <a name="blob_character_set-enumeration"></a>\_Enumerazione set di caratteri BLOB \_

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'enumerazione del **\_ \_ set di caratteri BLOB** indica il set di caratteri usato dal BLOB di conferenza corrente.

## <a name="syntax"></a>Sintassi


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**\_ASCII BCS**
</dt> <dd>

Formato ASCII standard.

</dd> <dt>

<span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**\_UTF7 BCS**
</dt> <dd>

Formato di trasformazione a sette bit di Unicode. Per informazioni dettagliate su questo formato, effettuare una ricerca Internet per RFC 1642.

</dd> <dt>

<span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**\_UTF8 BCS**
</dt> <dd>

Formato di trasformazione UCS 8. Per informazioni dettagliate su questo formato, eseguire una ricerca Internet per il documento ISO (il organizzazione internazionale per la standardizzazione) e IEC (il International Electrotechnical Commission) ISO/IEC JTC1/SC2/WG2 N 1036, data 1 agosto 1994, dall'editor di progetto WG2.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                               |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[**Ottieni \_ caratteri**](itconferenceblob-get-characterset.md)
</dt> <dt>

[**Init**](itconferenceblob-init.md)
</dt> <dt>

[**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 





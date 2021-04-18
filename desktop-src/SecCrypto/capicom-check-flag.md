---
description: Definisce le condizioni per cui deve essere controllata una catena di certificati.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: Enumerazione CAPICOM_CHECK_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CHECK_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 47b6168fb87ebbb65b07eadfe9adaf488934e252
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324913"
---
# <a name="capicom_check_flag-enumeration"></a>\_Enumerazione del flag di controllo CApicol \_

Il tipo di enumerazione del **\_ \_ flag di controllo CAPICOM** definisce le condizioni per cui deve essere controllata una catena di certificati.

## <a name="members"></a>Membri



| Membro                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Valore      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **\_controllo CAPICOM \_ None**                        | Non è stato eseguito alcun controllo di validità.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **capicot \_ controlla \_ radice attendibile \_**               | Verifica la presenza di una radice attendibile della catena di certificati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **\_validità controllo CApicol \_ \_**              | Verifica la validità dell'ora di tutti i certificati nella catena.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **validità della firma del \_ controllo CAPICOM \_ \_**         | Verifica se sono presenti firme valide per tutti i certificati della catena.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **\_verifica \_ stato di revoca online \_ \_ di CAPICOM**  | Controlla lo stato di revoca di tutti i certificati nella catena utilizzando gli elenchi di revoche di certificati (CRL) disponibili online. I CRL vengono scaricati utilizzando l'estensione del punto di distribuzione CRL (CDP) nel certificato. <br/> Se il CRL è stato scaricato e non è scaduto, CAPICOM lo usa e non passa alla rete. Se un CRL non è stato scaricato o non è aggiornato, CAPICOM passa online per tentare di scaricare il CRL.<br/> Questo flag viene ignorato se \_ \_ \_ \_ viene specificato anche lo stato di revoca offline del controllo CAPICOM.<br/> | 0x00000008 |
| **\_controlla \_ stato di revoca offline \_ \_ per CAPICOM** | Controlla lo stato di revoca di tutti i certificati nella catena utilizzando solo i CRL offline. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **sequenza di controllo di capicol \_ \_ completa \_**             | Controlla la catena completa. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **vincoli del nome del \_ controllo CAPICOM \_ \_**           | Verifica i vincoli del nome. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **i vincoli di \_ base del controllo CAPICOM \_ \_**          | Verifica i vincoli di base. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **\_ \_ periodo di validità nidificato del controllo \_ CAPICOM \_**    | Verifica la validità nidificata. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **capicot \_ controlla \_ \_ tutto online**                 | Controlla tutte le condizioni ad eccezione di \_ CAPICOM \_ controllare \_ lo stato di revoca offline \_ . I controlli di revoca vengono eseguiti su tutti i certificati nella catena, ad eccezione del certificato radice. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001EF |
| **controllo CAPICOM non \_ in \_ linea \_**                | Verifica tutte le condizioni ad eccezione di \_ CAPICOM \_ controllare \_ lo stato di revoca online \_ . I controlli di revoca vengono eseguiti su tutti i certificati nella catena, ad eccezione del certificato radice. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001F7 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 





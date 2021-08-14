---
description: Definisce le condizioni per cui deve essere verificata una catena di certificati.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: CAPICOM_CHECK_FLAG enumerazione (Capicom.h)
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
ms.openlocfilehash: 4b9fbc5ec1717acbd32c70ea3467465daf47de5d41af794a5164f44174a602d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772513"
---
# <a name="capicom_check_flag-enumeration"></a>Enumerazione CAPICOM \_ CHECK \_ FLAG

Il **tipo di enumerazione CAPICOM CHECK \_ \_ FLAG** definisce le condizioni per cui deve essere verificata una catena di certificati.

## <a name="members"></a>Membri



| Membro                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Valore      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ CHECK \_ NONE**                        | Non viene eseguito alcun controllo di validità.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **CAPICOM \_ CHECK \_ TRUSTED \_ ROOT**               | Verifica la presenza di una radice attendibile della catena di certificati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **VALIDITÀ \_ \_ DELL'ORA \_ DI CONTROLLO CAPICOM**              | Controlla la validità dell'ora di tutti i certificati nella catena.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **VERIFICA \_ DELLA \_ VALIDITÀ DELLA \_ FIRMA CAPICOM**         | Verifica la presenza di firme valide in tutti i certificati nella catena.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **CAPICOM \_ CHECK \_ ONLINE \_ REVOCATION \_ STATUS**  | Controlla lo stato di revoca di tutti i certificati nella catena usando gli elenchi di revoche di certificati (CRL) disponibili online. I CRL vengono scaricati usando l'estensione del punto di distribuzione CRL (CDP) nel certificato. <br/> Se l'elenco CRL è stato scaricato e non è scaduto, CAPICOM lo usa e non passa alla modalità online. Se un CRL non è stato scaricato o non è aggiornato, CAPICOM passa online per tentare di scaricare l'elenco CRL.<br/> Questo flag viene ignorato se viene specificato anche CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS.<br/> | 0x00000008 |
| **CAPICOM \_ CHECK \_ OFFLINE \_ REVOCATION \_ STATUS** | Controlla lo stato di revoca di tutti i certificati nella catena usando solo CRL offline. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **CAPICOM \_ CHECK \_ COMPLETE \_ CHAIN**             | Controlla la catena completa. Introdotto in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **VINCOLI DI NOME CHECK CAPICOM \_ \_ \_**           | Controlla i vincoli dei nomi. Introdotto in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **VINCOLI DI BASE \_ CAPICOM CHECK \_ \_**          | Controlla i vincoli di base. Introdotto in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **VERIFICA CAPICOM \_ \_ PERIODO DI \_ VALIDITÀ \_ ANNIDATO**    | Verifica la validità annidata. Introdotto in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **CAPICOM \_ CHECK \_ ONLINE \_ ALL**                 | Controlla tutte le condizioni ad eccezione di CAPICOM \_ CHECK \_ OFFLINE \_ \_ REVOCATION STATUS. I controlli di revoca vengono eseguiti su tutti i certificati della catena ad eccezione del certificato radice. Introdotto in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001EF |
| **CAPICOM \_ CHECK \_ OFFLINE \_ ALL**                | Controlla tutte le condizioni ad eccezione di CAPICOM \_ CHECK \_ ONLINE \_ \_ REVOCATION STATUS. I controlli di revoca vengono eseguiti su tutti i certificati della catena ad eccezione del certificato radice. Introdotto in CAPICOM 2.0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001F7 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 





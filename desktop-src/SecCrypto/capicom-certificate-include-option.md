---
description: Definisce quali certificati di una catena vengono salvati.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Enumerazione CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329737"
---
# <a name="capicom_certificate_include_option-enumeration"></a>\_ \_ Enumerazione dell'opzione Includi certificato capicol \_

Il tipo di enumerazione dell' **\_ \_ \_ opzione Includi certificato CAPICOM** definisce i certificati in una catena salvati. Questo tipo di enumerazione è stato introdotto in capicol 2,0.

## <a name="members"></a>Membri



| Membro                                                 | Descrizione                                                                           | Valore |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| **il certificato di \_ CAPICOM \_ include la \_ catena \_ ad eccezione della \_ radice** | Salva tutti i certificati nella catena con l'eccezione dell'entità radice.<br/> | 0     |
| **il certificato di \_ CAPICOM \_ include l' \_ intera \_ catena**        | Salva la catena di certificati completa.<br/>                                      | 1     |
| **il certificato capicol \_ \_ include \_ \_ solo entità finale \_**   | Salva solo il certificato dell'entità finale.<br/>                                     | 2     |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione dell' **\_ \_ \_ opzione di inclusione del certificato CAPICOM** viene utilizzato dal metodo [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 





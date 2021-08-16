---
description: Le costanti RENDBIND sono flag usati dal metodo ITDirectory::Bind per indicare i tipi di autenticazione forniti.
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: RENDBIND_ costanti (Rend.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c618ed2cf5d9dda4c2ee14b331e3603f8021e9c5f4755e38ecfb5929b5f45c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760864"
---
# <a name="rendbind_-constants"></a>Costanti \_ RENDBIND

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Le costanti RENDBIND sono flag usati dal metodo [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) per indicare i tipi di autenticazione forniti.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**AUTENTICAZIONE RENDBIND \_**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Autenticare l'utente.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTDOMAINNAME**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Usare il nome di dominio predefinito.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTUSERNAME**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Usare il nome utente predefinito.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTPASSWORD**
</dt> <dd> <dl> <dt>

 0x00000008
</dt> <dt>



Usare la password predefinita.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTCREDENTIALS**
</dt> <dd> <dl> <dt>

 0x0000000e
</dt> <dt>



I tre ORed precedenti sono stati uniti per praticità.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Rend.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 





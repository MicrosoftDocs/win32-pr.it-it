---
description: 'Le costanti RENDBIND sono flag usati dal metodo ITDirectory:: Bind per indicare i tipi di autenticazione forniti.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Costanti RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330741"
---
# <a name="rendbind_-constants"></a>\_Costanti RENDBIND

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Le costanti RENDBIND sono flag usati dal metodo [**ITDirectory:: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) per indicare i tipi di autenticazione forniti.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**\_autenticazione RENDBIND**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Autenticare l'utente.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**\_DEFAULTDOMAINNAME RENDBIND**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Usare il nome di dominio predefinito.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**\_DEFAULTUSERNAME RENDBIND**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Usare il nome utente predefinito.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**\_DEFAULTPASSWORD RENDBIND**
</dt> <dd> <dl> <dt>

 0x00000008
</dt> <dt>



Usa password predefinita.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**\_DEFAULTCREDENTIALS RENDBIND**
</dt> <dd> <dl> <dt>

 0x0000000E
</dt> <dt>



I tre ORed precedenti sono insieme per praticità.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Rend. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectory:: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 





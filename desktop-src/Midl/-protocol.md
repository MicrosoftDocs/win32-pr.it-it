---
title: opzione/Protocol
description: L'opzione/Protocol Specifica il protocollo wire supportato dallo stub generato.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /Protocol switch MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334660"
---
# <a name="protocol-switch"></a>opzione/Protocol

L'opzione **/Protocol** specifica il protocollo wire supportato dallo stub generato.

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>DCE * * * *


</dt> <dd>

Lo stub generato supporta solo il protocollo DCE.

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>ndr64****


</dt> <dd>

Lo stub generato supporta solo il protocollo Microsoft NDR64.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>tutti i * * * *


</dt> <dd>

Lo stub generato supporta tutti i protocolli disponibili per un determinato ambiente.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

RPC esegue il marshalling e l'unmarshalling dei dati in base a un protocollo di transito rigido, detto anche sintassi di trasferimento, che definisce la rappresentazione Wire di dati, ad esempio l'ordine in cui i membri dati vengono sottoposti a marshalling, l'allineamento dei dati in transito, informazioni aggiuntive incluse con i dati, tra gli altri. Microsoft RPC è compatibile con il protocollo OSF DCE (Network Data rappresentazione). Nella versione a 64 bit di Windows XP, Microsoft introduce un protocollo sperimentale NDR64 ottimizzato per il trasferimento dei dati a 64 bit. NDR64 non è compatibile con le versioni precedenti del protocollo DCE.

Il protocollo **DCE** è compatibile con la sintassi di trasferimento NDR di OSF DCE. Questo protocollo è ottimizzato per il trasferimento di dati a 32 bit.

Il protocollo **ndr64** è attualmente supportato solo se usato in combinazione con l'opzione [**/Win64**](-win64.md) . Se un client solo ndr64 tenta di connettersi a un server solo DCE, o viceversa, la chiamata viene rifiutata con la \_ \_ transazione SYN non supportata di RPC \_ \_ .

L'opzione **All** crea uno stub che può utilizzare qualsiasi protocollo disponibile. Per gli stub a 32 bit, l'unico protocollo attualmente disponibile è DCE. Per gli stub a 64 bit creati con l'opzione [**/Win64**](-win64.md) , sono disponibili sia DCE che NDR64.

## <a name="examples"></a>Esempio

**MIDL/Protocol all/Win64 filename. idl**

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 





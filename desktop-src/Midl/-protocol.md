---
title: Opzione /protocol
description: L'opzione /protocol specifica quale protocollo di rete è supportato dallo stub generato.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- Opzione /protocol MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555482677afff83d9f52e06c7b8e445504d222c8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887379"
---
# <a name="protocol-switch"></a>Opzione /protocol

**L'opzione /protocol** specifica quale protocollo di rete è supportato dallo stub generato.

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>dce****


</dt> <dd>

Lo stub generato supporta solo il protocollo DCE.

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>ndr64****


</dt> <dd>

Lo stub generato supporta solo il protocollo Microsoft NDR64.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>all****


</dt> <dd>

Lo stub generato supporta tutti i protocolli disponibili per un determinato ambiente.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

RPC effettua il marshalling e l'unmarshaling dei dati in base a un protocollo di trasmissione rigoroso, detto anche sintassi di trasferimento, che definisce la rappresentazione del collegamento dati, ad esempio l'ordine in cui i membri dati vengono sottoposti a marshalling, l'allineamento dei dati in transito, informazioni aggiuntive incluse con i dati, tra le altre. Microsoft RPC è compatibile con il protocollo NDR (network data representation) di OSF DCE. Nella versione a 64 bit di Windows XP, Microsoft introduce un protocollo sperimentale NDR64 ottimizzato per il trasferimento di dati a 64 bit. NDR64 non è compatibile con le versioni precedenti del protocollo DCE.

Il **protocollo dce** è compatibile con la sintassi di trasferimento NDR di OSF DCE. Questo protocollo è ottimizzato per il trasferimento di dati a 32 bit.

Il **protocollo ndr64** è attualmente supportato solo se usato in combinazione con l'opzione [**/win64.**](-win64.md) Se un client solo ndr64 tenta di connettersi a un server solo dce o viceversa, la chiamata viene rifiutata con RPC \_ S \_ UNSUPPORTED \_ TRANS \_ SYN.

**L'opzione all** crea uno stub che può usare qualsiasi protocollo disponibile. Per gli stub a 32 bit, l'unico protocollo attualmente disponibile è DCE. Per gli stub a 64 bit, creati con l'opzione [**/win64,**](-win64.md) sono disponibili sia DCE che NDR64.

## <a name="examples"></a>Esempio

**midl /protocol all /win64 filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/&lt;Sistema&gt;**](-system-.md)
</dt> </dl>

 

 





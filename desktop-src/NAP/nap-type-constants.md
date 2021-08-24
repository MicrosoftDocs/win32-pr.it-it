---
title: Costanti di tipo NAP (NapTypes.h)
description: Sono definite le costanti di Protezione accesso alla rete seguenti.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0201f29d19969de6050ce3eeebf29a7bee73792dcc6b61b2359e5660db12d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685921"
---
# <a name="nap-type-constants"></a>Costanti di tipo NAP

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Sono definite le costanti di Protezione accesso alla rete seguenti.

Le costanti nap seguenti sono definite in NapTypes.h:

<dl> <dt>

<span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**
</dt> <dd> <dl> <dt>

0x64
</dt> <dt>



Numero massimo di [**oggetti SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) associati a un [**pacchetto SoH.**](/windows/win32/api/naptypes/ns-naptypes-soh)


</dt> </dl> </dd> <dt>

<span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Dimensione massima, in byte, di un [**oggetto SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) associato a un pacchetto di istruzione di integrità ([**SoH).**](/windows/win32/api/naptypes/ns-naptypes-soh)


</dt> </dl> </dd> <dt>

<span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



Dimensione minima, in byte, di un [**pacchetto SoH.**](/windows/win32/api/naptypes/ns-naptypes-soh)


</dt> </dl> </dd> <dt>

<span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Dimensione massima, in byte, di un [**pacchetto SoH.**](/windows/win32/api/naptypes/ns-naptypes-soh)


</dt> </dl> </dd> <dt>

<span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/sizeof(DWORD)
</dt> <dt>



Numero massimo di valori DWORD associati a un [**oggetto SoHAttribute.**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)


</dt> </dl> </dd> <dt>

<span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x4
</dt> <dt>



Numero massimo di indirizzi IPv4 associati a un [**oggetto SoHAttribute.**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)


</dt> </dl> </dd> <dt>

<span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x10
</dt> <dt>



Numero massimo di indirizzi IPv6 associati a un [**oggetto SoHAttribute.**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)


</dt> </dl> </dd> <dt>

<span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



Lunghezza massima di una stringa specificata dalla [**struttura CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)


</dt> </dl> </dd> <dt>

<span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**
</dt> <dd> <dl> <dt>

(maxStringLength + 1) \* sizeof(WCHAR)
</dt> <dt>



Lunghezza massima, in byte, di una stringa specificata dalla [**struttura CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)


</dt> </dl> </dd> <dt>

<span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Numero massimo di entità di integrità del sistema, ad esempio SHV e SHA.


</dt> </dl> </dd> <dt>

<span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**
</dt> <dd> <dl> <dt>

\[range(0, maxSystemHealthEntityCount)\] 
</dt> <dt>



Intervallo di valori possibili per il numero di entità di integrità del sistema.


</dt> </dl> </dd> <dt>

<span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Numero massimo di entità di imposizione, ad esempio QEC.


</dt> </dl> </dd> <dt>

<span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**
</dt> <dd> <dl> <dt>

\[range(0, maxEnforcerCount)\]
</dt> <dt>



Intervallo di valori possibili per il numero di entità di imposizione.


</dt> </dl> </dd> <dt>

<span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**
</dt> <dd> <dl> <dt>

0xC8
</dt> <dt>



Dimensione massima, in byte, di una [**struttura PrivateData.**](/windows/win32/api/naptypes/ns-naptypes-privatedata)


</dt> </dl> </dd> <dt>

<span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Numero massimo di [**oggetti INapEnforcementClientConnection**](inapenforcementclientconnection.md) associati a un'entità di imposizione.


</dt> </dl> </dd> <dt>

<span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**
</dt> <dd> <dl> <dt>

maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer
</dt> <dt>



Numero massimo di connessioni SoH memorizzate nella cache per tutte le entità di integrità e imposizione del sistema.


</dt> </dl> </dd> <dt>

<span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Specifica che [**soHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)è dovuto a una nuova richiesta, non a una richiesta memorizzata nella cache. Questo flag viene usato dall'agente protezione accesso alla rete in [**un oggetto INapEnforcementClientConnection.**](inapenforcementclientconnection.md)


</dt> </dl> </dd> <dt>

<span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Specifica che è necessaria la correzione. Questo flag viene usato da un'applicazione SHA.


</dt> </dl> </dd> <dt>

<span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Numero di categorie di errori contenute in [**una struttura FailureCategoryMapping.**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Il componente è un client di imposizione della quarantena (QEC) che invia un [**pacchetto SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) in banda durante l'autenticazione della connessione.

> [!Note]  
> Questo valore non viene usato da SHAs e SHV.

 


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Il componente è un QEC che implementa [**INapCertRelyingParty**](inapcertrelyingparty.md) e deve interagire con il server dei certificati di integrità (HCS) per ottenere un certificato di integrità.

> [!Note]  
> Questo valore non viene usato da SHAs e SHV.

 


</dt> </dl> </dd> </dl>

Le costanti nap seguenti sono definite in NapEnforcementClient.h.

<dl> <dt>

<span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x0FA0
</dt> <dt>



Dimensione massima predefinita, in byte, di un pacchetto SoH.


</dt> </dl> </dd> <dt>

<span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**
</dt> <dd> <dl> <dt>

0xFFFF
</dt> <dt>



Dimensioni massime possibili, in byte, di un pacchetto SoH.


</dt> </dl> </dd> <dt>

<span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x012C
</dt> <dt>



Dimensioni massime minime possibili, in byte, di un pacchetto SoH. Le dimensioni effettive del pacchetto SoH possono essere inferiori a **minProtocolMaxSize**.


</dt> </dl> </dd> <dt>

<span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**
</dt> <dd> <dl> <dt>

range(minProtocolMaxSize, maxProtocolMaxSize)
</dt> <dt>



Intervallo di valori possibili per le dimensioni massime di un pacchetto SoH.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                                                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Costanti di Protezione accesso alla rete**](nap-constants.md)
</dt> </dl>

 

 






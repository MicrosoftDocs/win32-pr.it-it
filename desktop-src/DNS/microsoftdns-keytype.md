---
title: MicrosoftDNS_KEYType classe
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di risorse KEY.
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- MicrosoftDNS_KEYType DNS della classe
- MicrosoftDNS_KEYType classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279044856e695c7e287809a3cbe89a6fffbbc1c0352c0cb68ae45350aa17fc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109131"
---
# <a name="microsoftdns_keytype-class"></a>Classe \_ KeyType MicrosoftDNS

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di risorse KEY.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a>Members

La **classe \_ KEYType MicrosoftDNS** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ KEYType MicrosoftDNS** include questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un record di risorse KEY in base ai dati nei parametri di input del metodo: nome del server DNS del record, nome del contenitore, nome del proprietario, classe (impostazione predefinita = IN), valore di time-to-live e flag di mapping WINS, timeout di ricerca inversa, timeout della cache WINS e nome di dominio da aggiungere. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementati, statici<br/> |
| **Modifica**                         | Aggiorna la durata (TTL), il flag di mapping, il timeout di ricerca, il timeout della cache e il dominio dei risultati ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementati<br/>                          |



 

### <a name="properties"></a>Proprietà

La **classe \_ KEYType MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**Algoritmo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Algoritmo utilizzato con la chiave specificata nel record di risorse. I valori assegnati sono illustrati nella tabella seguente.



| Valore                                                                                                | Significato                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Crittografia a curva ellittica<br/> |



 

</dd> <dt>

**Flag**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Flag usati per specificare il mapping, come descritto in IETF RFC 2535.

</dd> <dt>

**Protocollo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo per il quale è possibile usare la chiave specificata nel record di risorse. I valori assegnati sono illustrati nella tabella seguente.



| Valore                                                                                                    | Significato                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | Posta elettronica<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | DNSSEC<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Tutti i protocolli<br/> |



 

</dd> <dt>

**PublicKey**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Chiave pubblica, rappresentata in base 64 come descritto nell'Appendice A di RFC 2535.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo CreateInstanceFromPropertyData della classe KEYType MicrosoftDNS \_**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della classe \_ KeyType MicrosoftDNS**](microsoftdns-keytype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






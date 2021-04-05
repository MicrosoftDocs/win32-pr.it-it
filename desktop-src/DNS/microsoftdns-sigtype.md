---
title: Classe MicrosoftDNS_SIGType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta un record di risorse di firma (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- DNS della classe MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740263"
---
# <a name="microsoftdns_sigtype-class"></a>\_Classe MicrosoftDNS SIGType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta un record di risorse di firma (SIG).

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a>Members

La **classe \_ SIGType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ SIGType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un RR SIG in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live e il flag di mapping WINS, il timeout della ricerca inversa, il timeout della cache WINS e il nome di dominio da aggiungere. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/>                                                                                                                                                                                                                                                       |
| **Modifica**                         | Aggiorna il valore TTL, il flag di mapping, il timeout di ricerca, il timeout della cache e il dominio dei risultati ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/> **Windows Server 2003:** Questo metodo aggiorna anche TypeCovered, Algorithm, labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName e Signature ai valori specificati come parametri di input di questo metodo.<br/> <br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ SIGType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**Algoritmo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Algoritmo utilizzato con la chiave specificata nel record di risorse. I valori assegnati sono riportati nella tabella seguente.



| Valore                                                                                                | Significato                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Crittografia a curva ellittica<br/> |



 

</dd> <dt>

**KeyTag**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Metodo usato per scegliere una chiave che verifica un SIG. Vedere RFC 2535, Appendice C per il metodo usato per calcolare un KeyTag.

</dd> <dt>

**Etichette**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Conteggio senza segno delle etichette nel nome originale del proprietario del record di firma. Il conteggio non include l'etichetta NULL per la radice, né i caratteri jolly iniziali.

</dd> <dt>

**OriginalTTL**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

TTL del set di RR firmato dal SIG.

</dd> <dt>

**Firma**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Firma, rappresentata in base 64, formattata come definito nella RFC 2535, Appendice A.

</dd> <dt>

**SignatureExpiration**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data di scadenza della firma, espressa in secondi dall'inizio del 1 gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.

</dd> <dt>

**SignatureInception**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora in cui la firma diventa valida, espressa in secondi a partire dall'inizio del 1 ° gennaio 1970, ora di Greenwich (GMT), esclusi i secondi intercalari.

</dd> <dt>

**SignerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di dominio del firmatario che ha generato il record SIG.

</dd> <dt>

**TypeCovered**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di RR coperto da questo SIG.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ SIGType**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe SIGType di MicrosoftDNS**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






---
title: Classe MicrosoftDNS_MXType
description: Sottoclasse di MicrosoftDNS \_ ResourceRecord che rappresenta uno scambio di posta elettronica (Mr) RR.
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- DNS della classe MicrosoftDNS_MXType
- MicrosoftDNS_MXType della classe DNS, descritta
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964222"
---
# <a name="microsoftdns_mxtype-class"></a>\_Classe MicrosoftDNS MXType

Sottoclasse di [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) che rappresenta uno scambio di posta elettronica (Mr) RR.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a>Members

La **classe \_ MXType di MicrosoftDNS** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ MXType di MicrosoftDNS** dispone di questi metodi.



| Metodo                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea un'istanza di un tipo MX di RR in base ai dati nei parametri di input del metodo: il nome del server DNS del record, il nome del contenitore, il nome del proprietario, la classe (impostazione predefinita = IN), il valore time-to-Live, la preferenza di record e il nome host disposti come scambio di posta elettronica. Restituisce un riferimento al nuovo oggetto come parametro di output. <br/> Qualificatori: implementata, statica<br/> |
| **Modifica**                         | Aggiorna la durata (TTL), la preferenza e lo scambio di posta elettronica ai valori specificati come parametri di input di questo metodo. Se non viene specificato un nuovo valore per un parametro, il valore corrente per il parametro non viene modificato. Il metodo restituisce un riferimento all'oggetto modificato come parametro di output. <br/> Qualificatori: implementato<br/>                         |



 

### <a name="properties"></a>Proprietà

La **classe \_ MXType di MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**MailExchange**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

FQDN che specifica un host disposto a fungere da scambio di posta elettronica per il nome del proprietario.

</dd> <dt>

**Preferenza**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Preferenza assegnata a questo RR tra gli altri nello stesso proprietario. Sono preferibili valori inferiori.

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

[**Metodo CreateInstanceFromPropertyData della classe MicrosoftDNS \_ MXType**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Metodo Modify della \_ classe MXType di MicrosoftDNS**](microsoftdns-mxtype-modify.md)
</dt> <dt>

[**\_ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






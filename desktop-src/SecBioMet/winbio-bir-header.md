---
title: Struttura WINBIO_BIR_HEADER ( \_ tipi WINBIO. h)
description: Contiene l'intestazione di un record di informazioni biometriche (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- Struttura di WINBIO_BIR_HEADER Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119783"
---
# <a name="winbio_bir_header-structure"></a>\_Struttura dell' \_ intestazione WINBIO Bir

La struttura dell' **\_ \_ intestazione WINBIO bir** contiene l'intestazione di un record di informazioni biometriche (Bir).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**ValidFields**
</dt> <dd>

Maschera di maschera che specifica i campi della struttura validi. Per altre informazioni, vedere [**\_ costanti di \_ campo WINBIO bir**](winbio-bir-field-constants.md).

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Costante **di \_ \_ versione di WINBIO bir** che specifica la versione dell'intestazione. I numeri di versione sono valori a 8 bit, dove i quattro bit più alti specificano il numero principale e i quattro bit bassi specificano il numero di versione secondario. Attualmente deve essere WINBIO \_ CBEFF \_ header \_ Version (0x11).

</dd> <dt>

**PatronHeaderVersion**
</dt> <dd>

Costante **di \_ \_ versione di WINBIO bir** che specifica la versione dell'intestazione. I numeri di versione sono valori a 8 bit, dove i quattro bit più alti specificano il numero principale e i quattro bit bassi specificano il numero di versione secondario. Attualmente deve essere WINBIO \_ patron \_ header \_ Version (0x11).

</dd> <dt>

**Flag dataflag**
</dt> <dd>

Valore che specifica il formato dei dati di intestazione. Può trattarsi di un **or** bit per bit dei flag del livello di sicurezza e di elaborazione seguenti. Per altre informazioni, vedere [**\_ \_ \_ costanti flag di dati WINBIO bir**](winbio-bir-data-flags-constants.md).



| Valore                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ \_ \_ Privacy del flag di dati**</dt> <dt>((UCHAR) 0x02)</dt> </dl>                                       | I dati sono crittografati.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ Integrità del flag di dati**</dt> <dt>((UCHAR) 0x01)</dt> </dl>                                 | I dati sono firmati digitalmente o protetti da un codice MAC (Message Authentication Code).<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ \_Flag data \_ firmato**</dt> <dt>((UCHAR) 0x04)</dt> </dl>                                          | Se vengono impostati questo flag e il flag di **\_ integrità del \_ flag \_ di dati WINBIO** , i dati vengono firmati. Se questo flag non è impostato ma è impostato il flag di **\_ integrità del \_ flag \_ di dati WINBIO** , viene calcolato un Mac sui dati.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ \_Flag dati \_ RAW**</dt> <dt>((UCHAR) 0x20)</dt> </dl>                                                   | I dati sono nel formato con cui sono stati acquisiti.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ FLAG di dati \_ \_ intermedio**</dt> <dt>((UCHAR) 0x40)</dt> </dl>                        | I dati non sono elaborati ma non sono stati completamente elaborati.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ FLAG di dati \_ \_ elaborati**</dt> <dt>((UCHAR) 0x80)</dt> </dl>                                 | I dati sono stati elaborati.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ \_Maschera di \_ opzione flag dati \_ \_ presente**</dt> <dt>((UCHAR) 0x08)</dt> </dl> | Il valore è sempre 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Tipo**
</dt> <dd>

\_Valore del tipo BIOmetrico WINBIO \_ che specifica il tipo di dati biometrici a cui si fa riferimento nel record di informazioni biometriche. Attualmente è supportata solo l' **\_ \_ impronta digitale di tipo WINBIO** . Per altre informazioni, vedere [**\_ costanti WINBIO di \_ tipo biometrico**](winbio-biometric-type-constants.md).

</dd> <dt>

**Subtype**
</dt> <dd>

Valore **del \_ \_ SOTTOtipo biometrico WINBIO** che specifica il Sottofattore associato ai dati biometrici. Per altre informazioni, vedere osservazioni e [**\_ \_ costanti SOTTOtipi biometrici WINBIO**](winbio-biometric-subtype-constants.md).

</dd> <dt>

**Scopo**
</dt> <dd>

Maschera **WINBIO \_ Bir \_ purpose** che specifica l'uso previsto dei dati. Può trattarsi di un **or** bit per bit dei valori seguenti. Per altre informazioni, vedere [**\_ costanti per \_ lo scopo di WINBIO bir**](winbio-bir-purpose-constants.md).

-   \_Verifica finalità \_ WINBIO
-   \_Identificazione scopo \_ WINBIO
-   \_registrazione scopo \_ WINBIO
-   \_registrazione scopo \_ WINBIO \_ per la \_ Verifica
-   \_registrazione scopo \_ WINBIO \_ per l' \_ Identificazione
-   \_controllo scopo \_ WINBIO

</dd> <dt>

**Dataquality**
</dt> <dd>

Valore che specifica la qualità relativa dei dati biometrici nel record di informazioni biometriche (BIR). Può essere un numero intero compreso tra 0 e 100 o uno dei valori seguenti. Per ulteriori informazioni, vedere [**WINBIO \_ Bir \_ Quality costanti**](winbio-bir-quality-constants.md).



| Valore                                                                                                                                                                                                                                                                                                        | Significato                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ DATA \_ Quality \_ Not \_ set**</dt> <dt>(( \_ qualità WINBIO bir \_ )-1)</dt> </dl>                   | Le misurazioni di qualità sono supportate dal creatore di BIR, ma in BIR non è impostato alcun valore.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ Qualità dei dati \_ \_ non \_ supportata**</dt> <dt>((WINBIO \_ Bir \_ Quality)-2)</dt> </dl> | Le misurazioni di qualità non sono supportate da BIR Creator.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

Data e ora, in formato UTC (ora di Greenwich), in cui è stato creato il BIR.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

Periodo per il quale BIR è valido.

<dl> <dt>

**BeginDate**
</dt> <dd>

Data e ora dell'inizio del periodo di validità dell'ora UTC (Coordinated Universal Time).

</dd> <dt>

**EndDate**
</dt> <dd>

Data e ora, in formato UTC (Coordinated Universal Time), in cui BIR cessa di essere valido.

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

Struttura [**di \_ \_ formato registrata WINBIO**](winbio-registered-format.md) che specifica il formato dati del blocco di dati standard nella struttura [**WINBIO \_ Bir**](winbio-bir.md) . I membri del **\_ \_ formato registrato WINBIO** non possono essere zero. Per semplificare il controllo degli errori, è possibile utilizzare le costanti seguenti.



| Valore                                                                                                                                                                                                                                                                                      | Significato                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_ Nessun \_ proprietario di formato \_ \_ disponibile**</dt> <dt>((ushort) 0)</dt> </dl> | Non è stato specificato alcun valore proprietario assegnato a IBROLI (International Biometric Industry Association).<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_ Nessun \_ tipo di formato \_ \_ disponibile**</dt> <dt>((ushort) 0)</dt> </dl>    | Non è stato specificato alcun tipo di formato.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Struttura [**di \_ \_ formato registrata WINBIO**](winbio-registered-format.md) che specifica l'ID prodotto del componente che ha generato il blocco di dati standard in Bir. I membri del **\_ \_ formato registrato WINBIO** possono essere pari a zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il parametro *SubType* specifica il Sottofattore associato ai dati biometrici. Attualmente, il Windows Biometric Framework (WBF) supporta solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sui sottotipi:

-   WINBIO \_ ANSI \_ 381 \_ POS \_ sconosciuta
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ pollice RH
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ - \_ dito indice
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ secondo \_ dito medio
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_ anulare
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ piccolo \_ dito
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito indice LH \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito medio SX \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ \_ dito sinistro
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ quattro \_ dita
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ quattro \_ dita
-   WINBIO \_ ANSI \_ 381 \_ POS \_ due \_ pollici

> [!IMPORTANT]
>
> Non tentare di convalidare il valore specificato per il valore del parametro del *sottotipo* . Il servizio biometria di Windows convaliderà il valore fornito prima di passarlo all'implementazione. Se il valore è **WINBIO, non vi sono \_ \_ \_ informazioni** o **\_ sottotipi \_ di WINBIO**, quindi eseguire la convalida laddove appropriato.

 

Se viene dichiarato uno dei bit seguenti, la struttura dell' **\_ \_ intestazione WINBIO bir** non è formattata correttamente.


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**\_Costanti SOTTOtipi BIOmetrici WINBIO \_**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**WINBIO \_ Bir**](winbio-bir.md)
</dt> <dt>

[**\_ \_ Costanti flag di dati WINBIO bir \_**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**\_Costanti di \_ campo WINBIO Bir**](winbio-bir-field-constants.md)
</dt> <dt>

[**Costanti WINBIO per \_ \_ finalità Bir**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**\_Costanti di \_ qualità WINBIO Bir**](winbio-bir-quality-constants.md)
</dt> <dt>

[**Costanti della versione di WINBIO \_ Bir \_**](winbio-bir-version-constants.md)
</dt> </dl>

 

 






---
title: WINBIO_BIR_HEADER struttura (Winbio \_ types.h)
description: Contiene l'intestazione di un record di informazioni biometriche (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- WINBIO_BIR_HEADER struttura Windows'API Biometric Framework
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
ms.openlocfilehash: d2166a206dd1590f83e16bc67482d3b42e24717efae4c44e54a99b9aa7d83b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911084"
---
# <a name="winbio_bir_header-structure"></a>Struttura WINBIO \_ BIR \_ HEADER

La **struttura WINBIO \_ BIR \_ HEADER** contiene l'intestazione di un record di informazioni biometriche (BIR).

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

**Campi validi**
</dt> <dd>

Maschera di bit che specifica quali campi della struttura sono validi. Per altre informazioni, vedere [**Costanti FIELD DI \_ WINBIO BIR. \_**](winbio-bir-field-constants.md)

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Costante **WINBIO \_ BIR \_ VERSION** che specifica la versione dell'intestazione. I numeri di versione sono valori a 8 bit in cui i quattro bit superiori specificano il numero principale e i quattro bit bassi specificano il numero di versione secondaria. Attualmente deve essere WINBIO \_ CBEFF \_ HEADER \_ VERSION (0x11).

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Costante **WINBIO \_ BIR \_ VERSION** che specifica la versione dell'intestazione. I numeri di versione sono valori a 8 bit in cui i quattro bit superiori specificano il numero principale e i quattro bit bassi specificano il numero di versione secondaria. Attualmente deve essere WINBIO \_ HEADER \_ VERSION \_ (0x11).

</dd> <dt>

**Flag di dati**
</dt> <dd>

Valore che specifica il formato dei dati dell'intestazione. Può trattarsi di **un'operazione OR** bit per bit dei flag del livello di sicurezza e di elaborazione seguenti. Per altre informazioni, vedere [**Costanti WINBIO \_ BIR \_ DATA \_ FLAGS.**](winbio-bir-data-flags-constants.md)



| Valore                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ PRIVACY \_ \_ DEI FLAG DI**</dt> DATI <dt>((UCHAR)0x02)</dt> </dl>                                       | I dati sono crittografati.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ INTEGRITÀ \_ DEI \_ FLAG DI**</dt> DATI <dt>((UCHAR)0x01)</dt> </dl>                                 | I dati sono firmati digitalmente o protetti da un codice MAC (Message Authentication Code).<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ SIGNED**</dt> <dt>((UCHAR)0x04)</dt> </dl>                                          | Se questo flag e il flag **WINBIO \_ DATA \_ FLAG \_ INTEGRITY** sono impostati, i dati vengono firmati. Se questo flag non è impostato ma è impostato il flag **WINBIO \_ DATA \_ FLAG \_ INTEGRITY,** viene calcolato un MAC sui dati.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ RAW**</dt> <dt>((UCHAR)0x20)</dt> </dl>                                                   | I dati sono nel formato con cui sono stati acquisiti.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt> </dl>                        | I dati non sono elaborati, ma non sono stati elaborati completamente.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ PROCESSED**</dt> <dt>((UCHAR)0x80)</dt> </dl>                                 | I dati sono stati elaborati.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG OPTION MASK \_ \_ \_ PRESENT**</dt> <dt>((UCHAR)0x08)</dt> </dl> | Il valore è sempre 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Tipo**
</dt> <dd>

Valore DI TIPO BIOMETRICO WINBIO che specifica il tipo di dati biometrici a cui si fa riferimento \_ nel record di informazioni \_ biometriche. Attualmente è **supportata solo l'impronta \_ digitale DI \_ TIPO WINBIO.** Per altre informazioni, vedere [**Costanti TYPE \_ BIOMETRIC \_ WINBIO.**](winbio-biometric-type-constants.md)

</dd> <dt>

**Sottotipo**
</dt> <dd>

Valore **\_ SUBTYPE BIOMETRIC \_ WINBIO** che specifica il fattore secondario associato ai dati biometrici. Per altre informazioni, vedere Osservazioni e Costanti [**\_ \_ SUBTYPE BIOMETRIC WINBIO.**](winbio-biometric-subtype-constants.md)

</dd> <dt>

**Scopo**
</dt> <dd>

Maschera **WINBIO \_ BIR \_ PURPOSE** che specifica l'uso previsto dei dati. Può trattarsi di **un'operazione OR** bit per bit dei valori seguenti. Per altre informazioni, vedere [**Costanti PURPOSE DI \_ WINBIO BIR. \_**](winbio-bir-purpose-constants.md)

-   VERIFICA DELLO SCOPO \_ WINBIO \_
-   IDENTIFICAZIONE DELLO SCOPO \_ WINBIO \_
-   REGISTRAZIONE PER SCOPO WINBIO \_ \_
-   REGISTRAZIONE A SCOPO \_ WINBIO \_ PER LA \_ \_ VERIFICA
-   REGISTRAZIONE ALLO SCOPO \_ WINBIO \_ PER \_ \_ L'IDENTIFICAZIONE
-   CONTROLLO SCOPO \_ WINBIO \_

</dd> <dt>

**DataQuality**
</dt> <dd>

Valore che specifica la qualità relativa dei dati biometrici nel record di informazioni biometriche (BIR). Può essere un numero intero compreso tra 0 e 100 o uno dei valori seguenti. Per altre informazioni, vedere [**Costanti \_ QUALITY \_ DI BIR WINBIO.**](winbio-bir-quality-constants.md)



| Valore                                                                                                                                                                                                                                                                                                        | Significato                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ QUALITÀ \_ DEI DATI NON \_ \_ IMPOSTATA**</dt> <dt>((QUALITÀ \_ BIR WINBIO)-1) \_</dt> </dl>                   | Le misurazioni di qualità sono supportate dall'autore di BIR, ma non è impostato alcun valore nel BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ QUALITÀ \_ DEI DATI NON \_ \_ SUPPORTATA**</dt> <dt>((QUALITÀ \_ BIR WINBIO)-2) \_</dt> </dl> | Le misurazioni di qualità non sono supportate dall'autore di BIR.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

Data e ora, in Coordinated Universal Time (Ora di Greenwich), in cui è stato creato il BIR.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

Periodo di validità del bir.

<dl> <dt>

**Begindate**
</dt> <dd>

Data e ora, in Coordinated Universal Time, di inizio del periodo di validità.

</dd> <dt>

**Enddate**
</dt> <dd>

Data e ora, in Coordinated Universal Time, in cui il bir smette di essere valido.

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

Struttura [**WINBIO \_ REGISTERED \_ FORMAT**](winbio-registered-format.md) che specifica il formato dati del blocco di dati standard nella [**struttura WINBIO \_ BIR.**](winbio-bir.md) I **membri DI WINBIO \_ REGISTERED \_ FORMAT** non possono essere zero. È possibile usare le costanti seguenti per semplificare il controllo degli errori.



| Valore                                                                                                                                                                                                                                                                                      | Significato                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_ NESSUN \_ PROPRIETARIO DI FORMATO \_ \_ DISPONIBILE**</dt> <dt>((USHORT)0)</dt> </dl> | Non è stato specificato alcun valore proprietario assegnato a IBIA (International Biometric Industry Association).<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_ NESSUN \_ TIPO \_ DI \_ FORMATO**</dt> <dt>DISPONIBILE ((USHORT)0)</dt> </dl>    | Non è stato specificato alcun tipo di formato.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Struttura [**WINBIO \_ REGISTERED \_ FORMAT**](winbio-registered-format.md) che specifica l'ID prodotto del componente che ha generato il blocco di dati standard nel BIR. I **membri DI WINBIO \_ REGISTERED \_ FORMAT** possono essere pari a zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il *parametro Subtype* specifica il fattore secondario associato ai dati biometrici. Attualmente, il Windows Biometric Framework (WBF) supporta solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sui sottotipi:

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS RH QUATTRO \_ \_ \_ DITA
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH QUATTRO \_ \_ DITA
-   WINBIO \_ ANSI \_ 381 \_ POS \_ TWO \_ THUMBS

> [!IMPORTANT]
>
> Non tentare di convalidare il valore fornito per il valore *del parametro Subtype.* Il Windows biometrica convalida il valore fornito prima di passarlo all'implementazione. Se il valore è **WINBIO \_ SUBTYPE \_ NO INFORMATION \_ o** **WINBIO \_ SUBTYPE \_ ANY,** convalidare dove appropriato.

 

Se viene asserito uno dei bit seguenti, il formato della struttura **WINBIO \_ BIR \_ HEADER** non è corretto.


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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**Costanti \_ SUBTYPE BIOMETRIC \_ WINBIO**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**WINBIO \_ BIR**](winbio-bir.md)
</dt> <dt>

[**Costanti WINBIO \_ BIR \_ DATA \_ FLAGS**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**Costanti FIELD \_ DI WINBIO BIR \_**](winbio-bir-field-constants.md)
</dt> <dt>

[**Costanti WINBIO \_ BIR \_ PURPOSE**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**Costanti QUALITY \_ DI BIR WINBIO \_**](winbio-bir-quality-constants.md)
</dt> <dt>

[**Costanti VERSION \_ di WINBIO BIR \_**](winbio-bir-version-constants.md)
</dt> </dl>

 

 






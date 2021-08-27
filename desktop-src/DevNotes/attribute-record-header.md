---
description: Rappresenta un record di attributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: ATTRIBUTE_RECORD_HEADER struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9664af36448bb125dc8d5fde3c4d22b04e58b1ca341acad561b94708acbf143c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045390"
---
# <a name="attribute_record_header-structure"></a>Struttura ATTRIBUTE \_ RECORD \_ HEADER

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta un record di attributo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**TypeCode**
</dt> <dd>

Codice del tipo di attributo.



| Valore                                                                                                                                                                                                                                           | Significato                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_ INFORMAZIONI**</dt> <dt>0x10</dt> </dl> | Attributi di file (ad esempio di sola lettura e archivio), timestamp ,ad esempio la creazione e l'ultima modifica del file, e il numero di collegamenti rigidi.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_ ELENCO**</dt> <dt>0x20</dt> </dl>                   | Elenco di attributi che costituiscono il file e il riferimento al file del record del file MFT in cui si trova ogni attributo.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_ NOME**</dt> <dt>0x30</dt> </dl>                                  | Nome del file, in caratteri Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_ Id**</dt> <dt>0x40</dt> </dl>                                  | Identificatore di oggetto a 64 byte assegnato dal servizio di rilevamento dei collegamenti.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$VOLUME \_ NOME**</dt> <dt>0x60</dt> </dl>                            | Etichetta del volume. Presente nel file $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$VOLUME \_ INFORMAZIONI**</dt> <dt>0x70</dt> </dl>       | Informazioni sul volume. Presente nel file $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$DATA**</dt> <dt>0x80</dt> </dl>                                                  | Contenuto del file.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$INDEX \_ Root**</dt> <dt>0x90</dt> </dl>                               | Usato per implementare l'allocazione dei nomi di file per directory di grandi dimensioni.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$INDEX \_ Allocazione**</dt> <dt>0xA0</dt> </dl>             | Usato per implementare l'allocazione dei nomi di file per directory di grandi dimensioni.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$BITMAP**</dt> <dt>0xB0</dt> </dl>                                            | Indice bitmap per una directory di grandi dimensioni.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ Punto**</dt> <dt>0xC0</dt> </dl>                      | Dati del reparse point.<br/>                                                                                                          |



 

</dd> <dt>

**Recordlength**
</dt> <dd>

Dimensione in byte del record dell'attributo. Questo valore riflette le dimensioni necessarie per la variante di record e viene sempre arrotondato al limite di quattro parole quadre più vicino.

</dd> <dt>

**FormCode**
</dt> <dd>

Codice del modulo dell'attributo.



| Valore                                                                                                                                                                                                                            | Significato                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**RESIDENTE \_ Modulo**</dt> <dt>0x00</dt> </dl>          | Il valore è contenuto nel record del file e segue immediatamente l'intestazione del record dell'attributo.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <dt>**NONRESIDENT \_ Modulo**</dt> <dt>0x01</dt> </dl> | Il valore è contenuto in altri settori del disco.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

Dimensione del nome dell'attributo facoltativo, in caratteri, oppure 0 se non è presente alcun nome di attributo. La lunghezza massima del nome dell'attributo è di 255 caratteri.

</dd> <dt>

**NameOffset**
</dt> <dd>

Offset del nome dell'attributo dall'inizio del record dell'attributo, in byte. Se il **membro NameLength** è 0, questo membro non è definito.

</dd> <dt>

**Flag**
</dt> <dd>

Flag di attributo.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE \_ FLAG \_ COMPRESSION \_ MASK** (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE \_ FLAG \_ SPARSE** (0x8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE \_ FLAG \_ CRITTOGRAFATO** (0x4000)
</dt> </dl> </dd> <dt>

**Istanza**
</dt> <dd>

Istanza univoca di questo attributo nel record del file.

</dd> <dt>

**Form**
</dt> <dd>

Se il **membro FormCode** è RESIDENT \_ FORM, l'unione è una **struttura Resident.** Se **FormCode è** NONRESIDENT \_ FORM, l'unione è una **struttura Nonresident.**

<dl> <dt>

**Residente**
</dt> <dd> <dl> <dt>

**ValueLength**
</dt> <dd>

Dimensione in byte del valore dell'attributo.

</dd> <dt>

**ValueOffset**
</dt> <dd>

Offset del valore dall'inizio del record dell'attributo, in byte.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> </dl> </dd> <dt>

**Non rientrante**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

Numero di cluster virtuale (VCN) più basso coperto da questo record di attributo.

</dd> <dt>

**HighestVcn**
</dt> <dd>

VcN più alto coperto da questo record di attributo.

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

Offset della matrice di coppie di mapping dall'inizio del record dell'attributo, in byte. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**AllocatedLength**
</dt> <dd>

Dimensioni allocate del file, in byte. Questo valore è un multiplo pari delle dimensioni del cluster. Questo membro non è valido se il **membro LowestVcn** è diverso da zero.

</dd> <dt>

**Dimensione**
</dt> <dd>

Dimensioni del file (byte più elevato che è possibile leggere più 1), in byte. Questo membro non è valido se **LowestVcn** è diverso da zero.

</dd> <dt>

**ValidDataLength**
</dt> <dd>

Lunghezza dei dati valida (byte inizializzati più 1), in byte. Questo valore viene arrotondato al limite del cluster più vicino. Questo membro non è valido se **LowestVcn** è diverso da zero.

</dd> <dt>

**TotalAllocated**
</dt> <dd>

Totale allocato per il file (somma dei cluster allocati).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e la versione secondaria 0 o 1, come segnalato da [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

I record degli attributi sono sempre allineati su un limite di quattro parole.

Se l'attributo non è rientrante, l'intestazione del record dell'attributo contiene un elenco di informazioni di recupero che fornisce un mapping tra vcn e numero di cluster logico (LCN) per l'attributo. Se le informazioni di recupero non rientrano nel segmento del file di base, possono essere archiviate in un segmento di record di file esterno da solo. Se non rientra ancora in un segmento di record di file esterno, nell'elenco degli attributi è presente un provisioning per contenere più voci per un attributo che richiedono informazioni di recupero aggiuntive.

La matrice di coppie di mapping viene archiviata in un formato compresso e presuppone che le informazioni siano decompresse e memorizzate nella cache dal sistema. È costituito da una serie di coppie NextVcn/CurrentLcn. Ad esempio, se un file ha una singola esecuzione di 8 cluster a partire da LCN 128 e il file inizia da LowestVcn 0, la matrice di coppie di mapping ha una sola voce, ovvero NextVcn=8 e CurrentLcn=128. La matrice è un flusso di byte che archivia le modifiche alle variabili di lavoro quando vengono elaborate in sequenza. Il flusso di byte deve essere interpretato come un flusso con terminazione zero di triple, come indicato di seguito:

count byte = *v* + (*l* \* 16)

dove *v* è il numero di byte vcn di basso ordine modificati e *l* è il numero di byte LCN modificati in ordine basso.

L'algoritmo di decompressione è il seguente:

1.  Inizializzare NextVcn su `Attribute->LowestVcn` e CurrentLcn su 0.
2.  Inizializzare il puntatore del flusso di byte su `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  Impostare CurrentVcn su NextVcn.
4.  Leggere il byte successivo dal flusso. Se è 0, interrompere. else *estrae v* *e l* come descritto in precedenza.
5.  Interpretare i *byte v successivi* come quantità con segno, con il byte di ordine più basso. Decomprimere l'estensione per l'accesso a 64 bit e aggiungerla a NextVcn.
6.  Interpretare i byte *l* successivi come una quantità con segno, con il byte più basso. Decomprimere l'estensione dell'accesso a 64 bit e aggiungerla a CurrentLcn. Se viene generato un valore CurrentLcn di 0, i vcn da CurrentVcn a NextVcn-1 non vengono allocati.
7.  Aggiornare le informazioni di mapping memorizzate nella cache da CurrentVcn, NextVcn e CurrentLcn.
8.  Andare al passaggio 3.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 

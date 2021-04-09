---
description: Rappresenta un record di attributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Struttura ATTRIBUTE_RECORD_HEADER
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
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877242"
---
# <a name="attribute_record_header-structure"></a>Struttura dell'intestazione del \_ record degli attributi \_

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
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_**</dt> <dt>0x10</dt> informazioni </dl> | Attributi di file (ad esempio di sola lettura e di archivio), timestamp (ad esempio, creazione di file e Ultima modifica) e conteggio dei collegamenti reali.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ ELENCAre**</dt> <dt>0x20</dt> </dl>                   | Elenco di attributi che compongono il file e il riferimento al file del record del file MFT in cui si trova ogni attributo.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ NOME**</dt> <dt>0x30</dt> </dl>                                  | Nome del file, in caratteri Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Identificatore di oggetto a 64 byte assegnato dal servizio di rilevamento dei collegamenti.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$Volume \_ NOME**</dt> <dt>0x60</dt> </dl>                            | Etichetta del volume. Presente nel file di $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$Volume \_**</dt> <dt>0x70</dt> informazioni </dl>       | Informazioni sul volume. Presente nel file di $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$Data**</dt> <dt>0x80</dt> </dl>                                                  | Contenuto del file.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$Index \_**</dt> <dt>0x90</dt> radice </dl>                               | Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$Index \_**</dt> <dt>Messaggi 0XA0</dt> di allocazione </dl>             | Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$Bitmap**</dt> <dt>0XB0</dt> </dl>                                            | Indice bitmap per una directory di grandi dimensioni.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ PUNTO**</dt> <dt>0xC0</dt> </dl>                      | Dati di reparse point.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

Dimensioni, in byte, del record di attributo. Questo valore riflette le dimensioni necessarie per la variante del record ed è sempre arrotondato al limite quadrupla più vicino.

</dd> <dt>

**FormCode**
</dt> <dd>

Codice del modulo dell'attributo.



| Valore                                                                                                                                                                                                                            | Significato                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**Residente \_ FORM**</dt> <dt>0x00</dt> </dl>          | Il valore è contenuto nel record del file e segue immediatamente l'intestazione del record dell'attributo.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> Non <dt>**residente \_ MODULO**</dt> <dt>0x01</dt> </dl> | Il valore è contenuto in altri settori del disco.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

Dimensioni del nome di attributo facoltativo, in caratteri, oppure 0 se non è presente alcun nome di attributo. La lunghezza massima del nome dell'attributo è di 255 caratteri.

</dd> <dt>

**NameOffset**
</dt> <dd>

Offset del nome dell'attributo dall'inizio del record di attributo, espresso in byte. Se il membro **NameLength** è 0, questo membro non è definito.

</dd> <dt>

**Flag**
</dt> <dd>

Flag di attributo.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Attributo \_ \_ \_ Maschera di compressione dei flag** (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Attributo \_ FLAG \_ sparse** (0x8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Attributo \_ FLAG \_ crittografato** (0x4000)
</dt> </dl> </dd> <dt>

**Istanza**
</dt> <dd>

Istanza univoca per questo attributo nel record di file.

</dd> <dt>

**Form**
</dt> <dd>

Se il membro **FormCode** è \_ un form residente, l'Unione è una struttura **residente** . Se **FormCode** è \_ un modulo non residente, l'Unione è una struttura non **residente** .

<dl> <dt>

**Residenti**
</dt> <dd> <dl> <dt>

**ValueLength**
</dt> <dd>

Dimensioni in byte del valore dell'attributo.

</dd> <dt>

**ValueOffset**
</dt> <dd>

Offset del valore dall'inizio del record di attributo, espresso in byte.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> </dl> </dd> <dt>

**Non residente**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

Il numero di cluster virtuale più basso (VCN) coperto da questo record di attributo.

</dd> <dt>

**HighestVcn**
</dt> <dd>

VCN più alto coperto da questo record di attributo.

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

Offset della matrice delle coppie di mapping dall'inizio del record di attributo, espresso in byte. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**AllocatedLength**
</dt> <dd>

Dimensione allocata del file, in byte. Questo valore è un multiplo pari delle dimensioni del cluster. Questo membro non è valido se il membro **LowestVcn** è diverso da zero.

</dd> <dt>

**FileSize**
</dt> <dd>

Dimensioni del file (byte più alto che possono essere lette più 1), in byte. Questo membro non è valido se **LowestVcn** è diverso da zero.

</dd> <dt>

**ValidDataLength**
</dt> <dd>

Lunghezza dei dati valida (byte più alto inizializzato più 1), in byte. Questo valore viene arrotondato al limite del cluster più vicino. Questo membro non è valido se **LowestVcn** è diverso da zero.

</dd> <dt>

**TotalAllocated**
</dt> <dd>

Totale allocato per il file (la somma dei cluster allocati).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

I record di attributo sono sempre allineati su un limite di quadrupla.

Se l'attributo non è residente, l'intestazione del record di attributo contiene un elenco di informazioni di recupero che forniscono un mapping tra VCN e il numero di cluster logico (LCN) per l'attributo. Se le informazioni di recupero non rientrano nel segmento di file di base, è possibile archiviarle in un segmento di record di file esterno. Se ancora non rientra in un segmento di record di file esterno, esiste un provisioning nell'elenco di attributi per contenere più voci per un attributo che richiede informazioni aggiuntive sul recupero.

La matrice di coppie di mapping è archiviata in un formato compresso e presuppone che le informazioni vengano decompresse e memorizzate nella cache dal sistema. È costituito da una serie di coppie NextVcn/CurrentLcn. Ad esempio, se un file ha una singola esecuzione di 8 cluster a partire da LCN 128 e il file inizia con LowestVcn 0, la matrice di coppie di mapping avrà solo una voce, ovvero NextVcn = 8 e CurrentLcn = 128. La matrice è un flusso di byte che archivia le modifiche apportate alle variabili di lavoro quando elaborate in sequenza. Il flusso di byte deve essere interpretato come un flusso con terminazione zero di tripli, come indicato di seguito:

conteggio byte = *v* + (*l* \* 16)

dove *v* è il numero di byte VCN di ordine inferiore modificati e *l* è il numero di byte LCN di ordine inferiore modificati.

L'algoritmo di decompressione è il seguente:

1.  Inizializzare NextVcn su `Attribute->LowestVcn` e CurrentLcn su 0.
2.  Inizializza il puntatore del flusso di byte in `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  Impostare CurrentVcn su NextVcn.
4.  Legge il byte successivo dal flusso. Se è 0, interrompere; altrimenti estrarre *v* e *l* come descritto in precedenza.
5.  Interpretare i successivi *v* byte come una quantità con segno, con prima il byte di ordine inferiore. Decomprimere il segno, esteso in 64 bit, e aggiungerlo a NextVcn.
6.  Interpretare i successivi *l* byte come una quantità con segno, con prima il byte di ordine inferiore. Decomprimere il segno, esteso in 64 bit, e aggiungerlo a CurrentLcn. Se l'oggetto produce un valore CurrentLcn pari a 0, il valore di VCNs da CurrentVcn a NextVcn-1 non è allocato.
7.  Aggiornare le informazioni di mapping memorizzate nella cache da CurrentVcn, NextVcn e CurrentLcn.
8.  Andare al passaggio 3.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 

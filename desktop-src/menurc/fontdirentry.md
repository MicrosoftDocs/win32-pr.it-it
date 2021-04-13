---
title: Struttura FONTDIRENTRY
description: Contiene informazioni su un singolo tipo di carattere in un gruppo di risorse dei tipi di carattere. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menu struttura FONTDIRENTRY e altre risorse
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475772"
---
# <a name="fontdirentry-structure"></a>Struttura FONTDIRENTRY

Contiene informazioni su un singolo tipo di carattere in un gruppo di risorse dei tipi di carattere. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**dfVersion**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di versione definito dall'utente per i dati della risorsa che gli strumenti possono usare per leggere e scrivere i file di risorse.

</dd> <dt>

**dfSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni, in byte, del file.

</dd> <dt>

**dfCopyright \[ 60\]**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Informazioni sul copyright del fornitore di tipi di carattere.

</dd> <dt>

**dfType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tipo di file del tipo di carattere.

</dd> <dt>

**dfPoints**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Dimensioni del punto in cui il set di caratteri è migliore.

</dd> <dt>

**dfVertRes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Risoluzione verticale, espressa in punti per pollice, in cui il set di caratteri è stato digitato.

</dd> <dt>

**dfHorizRes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Risoluzione orizzontale, espressa in punti per pollice, in cui il set di caratteri è stato digitato.

</dd> <dt>

**dfAscent**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Distanza tra la parte superiore di una cella di definizione dei caratteri e la linea di base del tipo di carattere tipografico.

</dd> <dt>

**dfInternalLeading**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Quantità di iniziali all'interno dei limiti impostati dal membro **dfPixHeight** . In quest'area possono essere presenti contrassegni accentati e altri caratteri diacritici.

</dd> <dt>

**dfExternalLeading**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Quantità di porta aggiuntiva che l'applicazione aggiunge tra le righe.

</dd> <dt>

**dfItalic**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Un tipo di carattere corsivo se non uguale a zero.

</dd> <dt>

**dfUnderline**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Carattere sottolineato se non uguale a zero.

</dd> <dt>

**dfStrikeOut**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Un tipo di carattere di attacco se non è uguale a zero.

</dd> <dt>

**dfWeight**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Spessore del tipo di carattere nell'intervallo compreso tra 0 e 1000. 400, ad esempio, è Roman e 700 è in grassetto. Se questo valore è zero, viene utilizzato un peso predefinito. Per altri valori definiti, vedere la descrizione della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfCharSet**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Set di caratteri del tipo di carattere. Per i valori predefiniti, vedere la descrizione della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfPixWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Larghezza della griglia in cui è stato digitato un tipo di carattere vettoriale. Per i tipi di carattere raster, se il membro non è uguale a zero, rappresenta la larghezza per tutti i caratteri nella bitmap. Se il membro è uguale a zero, il tipo di carattere ha caratteri a larghezza variabile.

</dd> <dt>

**dfPixHeight**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Altezza della bitmap dei caratteri per i tipi di carattere raster o l'altezza della griglia in cui è stato digitalizzato un tipo di carattere vettoriale.

</dd> <dt>

**dfPitchAndFamily**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Il pitch e la famiglia del tipo di carattere. Per ulteriori informazioni, vedere la descrizione della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfAvgWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Larghezza media dei caratteri nel tipo di carattere, generalmente definita come larghezza della lettera x. Questo valore non include la sporgenza richiesta per i caratteri in grassetto o in corsivo.

</dd> <dt>

**dfMaxWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Larghezza del carattere più largo nel tipo di carattere.

</dd> <dt>

**dfFirstChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Primo codice carattere definito nel tipo di carattere.

</dd> <dt>

**dfLastChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Ultimo codice carattere definito nel tipo di carattere.

</dd> <dt>

**dfDefaultChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Carattere da sostituire per i caratteri non presenti nel tipo di carattere.

</dd> <dt>

**dfBreakChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Carattere che verrà utilizzato per definire le interruzioni di parola per la giustificazione del testo.

</dd> <dt>

**dfWidthBytes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di byte in ogni riga della bitmap. Questo valore è sempre pari, in modo che le righe vengano avviate sui limiti di parola. Per i tipi di carattere vettoriali, questo membro non ha alcun significato.

</dd> <dt>

**dfDevice**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Offset nel file a una stringa con terminazione null che specifica il nome di un dispositivo. Per un tipo di carattere generico, questo valore è zero.

</dd> <dt>

**dfFace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Offset nel file a una stringa con terminazione null che denomina il carattere tipografico.

</dd> <dt>

**dfReserved**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Questo membro è riservato.

</dd> <dt>

**szDeviceName**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Nome del dispositivo se il file del tipo di carattere è designato per un dispositivo specifico.

</dd> <dt>

**szFaceName**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Nome tipografico del tipo di carattere.

</dd> </dl>

## <a name="remarks"></a>Commenti

Esiste una struttura **FONTDIRENTRY** per ogni tipo di carattere nel file res. Le applicazioni che generano file con estensione res con le risorse del tipo di carattere devono anche aggiungere al file una struttura **FONTDIRENTRY** per ogni tipo di carattere.

Le dichiarazioni dei tipi di carattere possono essere combinate con altre dichiarazioni di risorse in. File RC perché non è necessario che i tipi di carattere siano contigui nel file res.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Diaffitto**](direntry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 


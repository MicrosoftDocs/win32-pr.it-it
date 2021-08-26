---
title: Struttura FONTDIRENTRY
description: Contiene informazioni su un singolo tipo di carattere in un gruppo di risorse del tipo di carattere. La definizione della struttura fornita qui è solo a solo supporto della spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Struttura FONTDIRENTRY Menu e altre risorse
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e236104730dbbfe79ec0ed3d18cbb465402ed8827c6037a2457bec18faf63024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886741"
---
# <a name="fontdirentry-structure"></a>Struttura FONTDIRENTRY

Contiene informazioni su un singolo tipo di carattere in un gruppo di risorse del tipo di carattere. La definizione della struttura fornita qui è solo a solo supporto della spiegazione. non è presente in alcun file di intestazione standard.

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

Tipo: **WORD**

</dd> <dd>

Numero di versione definito dall'utente per i dati delle risorse che gli strumenti possono usare per leggere e scrivere i file di risorse.

</dd> <dt>

**dfSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni del file, in byte.

</dd> <dt>

**dfCopyright \[ 60\]**
</dt> <dd>

Tipo: **CHAR**

</dd> <dd>

Informazioni sul copyright del fornitore del tipo di carattere.

</dd> <dt>

**dfType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo di file del tipo di carattere.

</dd> <dt>

**dfPoints**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Dimensione in punti in base alla quale il set di caratteri ha un aspetto migliore.

</dd> <dt>

**dfVertRes**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Risoluzione verticale, in punti per pollice, in corrispondenza della quale è stato digitalizzato questo set di caratteri.

</dd> <dt>

**dfHorizRes**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Risoluzione orizzontale, in punti per pollice, in corrispondenza della quale è stato digitalizzato questo set di caratteri.

</dd> <dt>

**dfAscent**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Distanza dalla parte superiore di una cella di definizione del carattere alla linea di base del tipo di carattere tipografico.

</dd> <dt>

**dfInternalLeading**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Quantità di iniziale all'interno dei limiti impostati dal **membro dfPixHeight.** In quest'area possono essere presenti segni accentati e altri caratteri diacritici.

</dd> <dt>

**dfExternalLeading**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Quantità di spazio iniziale aggiuntivo che l'applicazione aggiunge tra le righe.

</dd> <dt>

**dfItalic**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Carattere corsivo se diverso da zero.

</dd> <dt>

**dfUnderline**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Carattere sottolineato se diverso da zero.

</dd> <dt>

**dfStrikeOut**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Carattere barrato se diverso da zero.

</dd> <dt>

**dfWeight**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Spessore del tipo di carattere compreso tra 0 e 1000. Ad esempio, 400 è roman e 700 è in grassetto. Se questo valore è zero, viene usato un peso predefinito. Per altri valori definiti, vedere la descrizione della [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfCharSet**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Set di caratteri del tipo di carattere. Per i valori predefiniti, vedere la descrizione della [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfPixWidth**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Larghezza della griglia in cui è stato digitalizzato un tipo di carattere vettoriale. Per i tipi di carattere raster, se il membro non è uguale a zero, rappresenta la larghezza per tutti i caratteri nella bitmap. Se il membro è uguale a zero, il tipo di carattere include caratteri a larghezza variabile.

</dd> <dt>

**dfPixHeight**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Altezza della bitmap del carattere per i tipi di carattere raster o altezza della griglia in cui è stato digitalizzato un tipo di carattere vettoriale.

</dd> <dt>

**dfPitchAndFamily**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Passo e famiglia del tipo di carattere. Per altre informazioni, vedere la descrizione della [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfAvgWidth**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Larghezza media dei caratteri nel tipo di carattere (in genere definita come larghezza della lettera x). Questo valore non include l'overhang necessario per i caratteri in grassetto o corsivo.

</dd> <dt>

**dfMaxWidth**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Larghezza del carattere più largo nel tipo di carattere.

</dd> <dt>

**dfFirstChar**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Primo codice carattere definito nel tipo di carattere.

</dd> <dt>

**dfLastChar**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Ultimo codice carattere definito nel tipo di carattere.

</dd> <dt>

**dfDefaultChar**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Carattere da sostituire ai caratteri non presenti nel tipo di carattere.

</dd> <dt>

**dfBreakChar**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Carattere che verrà usato per definire le interruzioni di parola per la giustificazione del testo.

</dd> <dt>

**dfWidthBytes**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Numero di byte in ogni riga della bitmap. Questo valore è sempre pari in modo che le righe inizino in base ai limiti delle parole. Per i tipi di carattere vettoriali, questo membro non ha alcun significato.

</dd> <dt>

**dfDevice**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Offset nel file in una stringa con terminazione Null che specifica il nome di un dispositivo. Per un tipo di carattere generico, questo valore è zero.

</dd> <dt>

**dfFace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Offset nel file in una stringa con terminazione Null che indica il nome del carattere tipografico.

</dd> <dt>

**dfReserved**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Questo membro è riservato.

</dd> <dt>

**szDeviceName**
</dt> <dd>

Tipo: **CHAR**

</dd> <dd>

Nome del dispositivo se il file del tipo di carattere è designato per un dispositivo specifico.

</dd> <dt>

**szFaceName**
</dt> <dd>

Tipo: **CHAR**

</dd> <dd>

Nome del carattere tipografico del tipo di carattere.

</dd> </dl>

## <a name="remarks"></a>Commenti

Esiste una struttura **FONTDIRENTRY** per ogni tipo di carattere nel file con estensione res. Anche le applicazioni che generano file res con risorse del tipo di carattere devono aggiungere al file **una struttura FONTDIRENTRY** per ogni tipo di carattere.

Le dichiarazioni dei tipi di carattere possono essere miste con altre dichiarazioni di risorse in . File RC perché i tipi di carattere non devono essere contigui nel file con estensione res.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 


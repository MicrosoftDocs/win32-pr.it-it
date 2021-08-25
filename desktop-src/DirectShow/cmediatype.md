---
description: La classe CMediaType gestisce i tipi di supporti. Questa classe eredita la struttura AM \_ MEDIA \_ TYPE. È possibile eseguire il cast a una variabile di tipo AM \_ MEDIA \_ TYPE.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Classe CMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49680848fc764cdbbdfeaf3bea363f29427a745297ef4fb39bca09159aa582f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831947"
---
# <a name="cmediatype-class"></a>Classe CMediaType

![Gerarchia di classi cmediatype](images/mtype01.png)

La `CMediaType` classe gestisce i tipi di supporti. Questa classe eredita la [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) È possibile eseguire il cast a una variabile di tipo **AM \_ MEDIA \_ TYPE**.



| Metodi pubblici                                                      | Descrizione                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CMediaType**](cmediatype-cmediatype.md)                         | Metodo del costruttore.                                                            |
| [**~CMediaType**](cmediatype--cmediatype.md)                       | Metodo del distruttore.                                                             |
| [**Impostare**](cmediatype-set.md)                                       | Imposta il tipo di supporto da un altro tipo di supporto.                                   |
| [**isValid**](cmediatype-isvalid.md)                               | Determina se a questo oggetto è stato assegnato un tipo principale.              |
| [**Tipo**](cmediatype-type.md)                                     | Recupera il tipo principale.                                                      |
| [**SetType**](cmediatype-settype.md)                               | Specifica il tipo principale.                                                      |
| [**Sottotipo**](cmediatype-subtype.md)                               | Recupera il sottotipo.                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | Specifica il sottotipo.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Determina se gli esempi hanno dimensioni fisse o variabili.                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | Determina se il flusso usa la compressione temporale.                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | Recupera le dimensioni del campione.                                                     |
| [**SetSampleSize**](cmediatype-setsamplesize.md)                   | Specifica una dimensione fissa del campione o specifica che i campioni hanno dimensioni variabili. |
| [**SetVariableSize**](cmediatype-setvariablesize.md)               | Specifica che gli esempi non hanno dimensioni fisse.                               |
| [**SetTemporalCompression**](cmediatype-settemporalcompression.md) | Specifica se i campioni vengono compressi usando la compressione temporale.           |
| [**Formato**](cmediatype-format.md)                                 | Recupera un puntatore al blocco di formato.                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | Recupera la lunghezza del blocco di formato.                                      |
| [**SetFormatType**](cmediatype-setformattype.md)                   | Specifica il tipo di formato.                                                     |
| [**Formattype**](cmediatype-formattype.md)                         | Recupera il tipo di formato.                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | Specifica il blocco di formato.                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | Elimina il blocco di formato.                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | Alloca memoria per il blocco di formato.                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | Rialloca il blocco di formato a una nuova dimensione.                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | Inizializza il tipo di supporto.                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | Determina se questo tipo di supporto corrisponde a un tipo di supporto parzialmente specificato.        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | Determina se il tipo di supporto è parzialmente definito.                             |
| Operatori                                                           | Descrizione                                                                    |
| [**operatore =**](cmediatype-operator-.md)                          | Esegue l'overload dell'operatore di assegnazione per copiare un tipo di supporto.                        |
| [**operatore ==**](cmediatype-operator--.md)                        | Verifica l'uguaglianza tra oggetti `CMediaType`.                               |
| [**operatore !=**](cmediatype-operator-neq.md)                      | Verifica la disuguaglianza tra oggetti `CMediaType`.                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 





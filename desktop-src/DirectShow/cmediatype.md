---
description: La classe CMediaType gestisce i tipi di supporto. Questa classe eredita la \_ struttura del tipo di supporto am \_ . È possibile eseguire il cast a una variabile di tipo AM \_ media \_ Type.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Classe CMediaType (mtype. h)
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
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327450"
---
# <a name="cmediatype-class"></a>Classe CMediaType

![gerarchia di classi CMediaType](images/mtype01.png)

La `CMediaType` classe gestisce i tipi di supporto. Questa classe eredita la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . È possibile eseguire il cast a una variabile di tipo **am \_ media \_ Type**.



| Metodi pubblici                                                      | Descrizione                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CMediaType**](cmediatype-cmediatype.md)                         | Metodo del costruttore.                                                            |
| [**~ CMediaType**](cmediatype--cmediatype.md)                       | Metodo del distruttore.                                                             |
| [**Set**](cmediatype-set.md)                                       | Imposta il tipo di supporto da un altro tipo di supporto.                                   |
| [**isValid**](cmediatype-isvalid.md)                               | Determina se un tipo principale è stato assegnato a questo oggetto.              |
| [**Tipo**](cmediatype-type.md)                                     | Recupera il tipo principale.                                                      |
| [**SetType**](cmediatype-settype.md)                               | Specifica il tipo principale.                                                      |
| [**Subtype**](cmediatype-subtype.md)                               | Recupera il sottotipo.                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | Specifica il sottotipo.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Determina se gli esempi hanno dimensioni fisse o variabili.                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | Determina se il flusso usa la compressione temporale.                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | Recupera le dimensioni del campione.                                                     |
| [**SetSampleSize**](cmediatype-setsamplesize.md)                   | Specifica una dimensione del campione fissa o specifica che gli esempi hanno una dimensione variabile. |
| [**SetVariableSize**](cmediatype-setvariablesize.md)               | Specifica che gli esempi non hanno dimensioni fisse.                               |
| [**SetTemporalCompression**](cmediatype-settemporalcompression.md) | Specifica se gli esempi vengono compressi con la compressione temporale.           |
| [**Formato**](cmediatype-format.md)                                 | Recupera un puntatore al blocco di formato.                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | Recupera la lunghezza del blocco di formato.                                      |
| [**SetFormatType**](cmediatype-setformattype.md)                   | Specifica il tipo di formato.                                                     |
| [**FormatType**](cmediatype-formattype.md)                         | Recupera il tipo di formato.                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | Specifica il blocco di formato.                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | Elimina il blocco di formato.                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | Alloca memoria per il blocco di formato.                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | Rialloca il blocco di formato in una nuova dimensione.                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | Inizializza il tipo di supporto.                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | Determina se questo tipo di supporto corrisponde a un tipo di supporto parzialmente specificato.        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | Determina se il tipo di supporto è parzialmente definito.                             |
| Operatori                                                           | Descrizione                                                                    |
| [**operatore =**](cmediatype-operator-.md)                          | Consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.                        |
| [**operatore = =**](cmediatype-operator--.md)                        | Verifica l'uguaglianza tra oggetti `CMediaType`.                               |
| [**operatore! =**](cmediatype-operator-neq.md)                      | Verifica la disuguaglianza tra oggetti `CMediaType`.                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 





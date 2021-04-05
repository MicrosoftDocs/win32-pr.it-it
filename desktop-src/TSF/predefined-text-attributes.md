---
title: Attributi di testo predefiniti (TsAttrid. h)
description: I valori seguenti identificano gli attributi di testo ottenuti con il metodo ITfContext GetAppProperty. Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.
ms.assetid: af73edb8-b706-40e4-a093-4ac22d33ecdc
keywords:
- Framework servizi di testo attributi di testo predefiniti
topic_type:
- apiref
api_name:
- Predefined Text Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cb214f6c555b589c52e9916325e38b46b0bfb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120906"
---
# <a name="predefined-text-attributes"></a>Attributi di testo predefiniti

I valori seguenti identificano gli attributi di testo ottenuti con il metodo [**ITfContext:: GetAppProperty**](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.

## <a name="properties"></a>Proprietà



| Proprietà                                     | Descrizione                                                                                                                                              |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Testo TSATTRID                               | Non usato.                                                                                                                                                |
| \_Allineamento del testo TSATTRID \_                    | Non usato.                                                                                                                                                |
| \_ \_ Centro allineamento testo \_ TSATTRID            | Contiene un valore diverso da zero se il testo è centrato o zero in caso contrario.                                                                                      |
| \_Allineamento del testo TSATTRID \_ \_ giustificato           | Contiene un valore diverso da zero se il testo è giustificato o zero in caso contrario.                                                                                     |
| \_Allineamento testo TSATTRID a \_ \_ sinistra              | Contiene un valore diverso da zero se il testo è allineato a sinistra o zero in caso contrario.                                                                                  |
| \_Allineamento testo TSATTRID a \_ \_ destra             | Contiene un valore diverso da zero se il testo è allineato a destra o zero in caso contrario.                                                                                 |
| \_EmbeddedObject testo \_ TSATTRID               | Contiene un valore diverso da zero se il testo è un oggetto incorporato o zero in caso contrario.                                                                            |
| \_Sillabazione del testo TSATTRID \_                  | Contiene un valore diverso da zero se il testo è con trattino o zero in caso contrario.                                                                                    |
| \_Lingua del testo TSATTRID \_                     | Contiene l'identificatore di lingua **LangID** del testo.                                                                                                 |
| \_Collegamento di testo TSATTRID \_                         | Contiene un puntatore a un oggetto collegamento. Il chiamante deve usare il metodo QueryInterface per ottenere l'interfaccia desiderata, ad esempio **IUniformResourceLocator**. |
| \_Orientamento del testo TSATTRID \_                  | Specifica l'angolo, in decimi di gradi, tra la linea di base del testo e l'asse x del dispositivo.                                                          |
| TSATTRID \_ testo \_ para                         | Non usato.                                                                                                                                                |
| TSATTRID \_ Text \_ para \_ FirstLineIndent        | Contiene il numero di punti in cui viene rientrata la prima riga di un paragrafo.                                                                            |
| TSATTRID \_ Text \_ para \_ LeftIndent             | Contiene il numero di punti a partire dal quale il paragrafo viene rientrato.                                                                              |
| TSATTRID \_ Text \_ para \_ LineSpacing            | Non usato.                                                                                                                                                |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ atleast   | Contiene il numero minimo di righe per l'interlinea del paragrafo.                                                                              |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ Double    | Contiene un valore diverso da zero se il paragrafo è con uno spazio doppio o zero in caso contrario.                                                                            |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ esattamente   | Contiene il numero esatto di righe per l'interlinea del paragrafo.                                                                                |
| TSATTRID \_ testo \_ para \_ LineSpacing \_ più  | Contiene il numero di righe per la spaziatura tra più righe del paragrafo.                                                                             |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ OnePtFive | Contiene un valore diverso da zero se il paragrafo è uno e uno a metà spaziatura o zero in caso contrario.                                                             |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ Single    | Contiene un valore diverso da zero se il paragrafo è con spaziatura singola o zero in caso contrario.                                                                            |
| TSATTRID \_ Text \_ para \_ RightIndent            | Contiene il numero di punti per i quali il paragrafo viene rientrato da destra.                                                                             |
| TSATTRID \_ Text \_ para \_ SpaceAfter             | Contiene il numero di punti di spaziatura dopo il paragrafo.                                                                                            |
| TSATTRID \_ Text \_ para \_ SpaceBefore            | Contiene il numero di punti di spaziatura prima del paragrafo.                                                                                           |
| TSATTRID \_ testo \_ ReadOnly                     | Contiene zero se il testo è di sola lettura o diverso da zero.                                                                                             |
| \_RightToLeft testo \_ TSATTRID                  | Contiene zero se il testo è di lettura da destra a sinistra o diverso da zero.                                                                                 |
| \_VerticalWriting testo \_ TSATTRID              | Specifica se il testo è verticale o orizzontale. Contiene zero se il testo è orizzontale o diverso da zero se il testo è verticale.                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



 


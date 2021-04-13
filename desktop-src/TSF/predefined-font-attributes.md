---
title: Attributi del tipo di carattere predefiniti (TsAttrid. h)
description: I valori seguenti identificano gli attributi del tipo di carattere ottenuti con il metodo GetAppProperty di ITfContext. Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.
ms.assetid: 8d73c258-77d5-46db-9d31-ac41d9e7acb3
keywords:
- Framework dei servizi di testo attributi del tipo di carattere predefiniti
topic_type:
- apiref
api_name:
- Predefined Font Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21351d790a09c9364a101a62b7516698df154225
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340982"
---
# <a name="predefined-font-attributes"></a>Attributi del tipo di carattere predefiniti

I valori seguenti identificano gli attributi del tipo di carattere ottenuti con il metodo [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.

## <a name="properties"></a>Proprietà



| Proprietà                                                 | Descrizione                                                                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **\_Tipo di carattere TSATTRID**                                       | Non usato.                                                                                                                   |
| **\_Tipo di carattere TSATTRID \_**                             | Contiene il nome del tipo di carattere del testo.                                                                                    |
| **\_SizePts del tipo di carattere TSATTRID \_**                              | Contiene la dimensione in punti del tipo di carattere del testo.                                                                                   |
| **\_Stile del tipo di carattere TSATTRID \_**                                | Non usato.                                                                                                                   |
| **\_ \_ Animazione dello stile del tipo di carattere TSATTRID \_**                     | Non usato.                                                                                                                   |
| **\_Animazione dello stile del tipo di carattere TSATTRID \_ \_ \_ BlinkingBackground** | Contiene un valore diverso da zero se il testo ha l'animazione specificata o zero in caso contrario.                                         |
| **\_Animazione dello stile del tipo di carattere TSATTRID \_ \_ \_ LasVegasLights**     | Contiene un valore diverso da zero se il testo ha l'animazione specificata o zero in caso contrario.                                         |
| **\_Animazione dello stile del tipo di carattere TSATTRID \_ \_ \_ MarchingBlackAnts**  | Contiene un valore diverso da zero se il testo ha l'animazione specificata o zero in caso contrario.                                         |
| **\_Animazione dello stile del tipo di carattere TSATTRID \_ \_ \_ MarchingRedAnts**    | Contiene un valore diverso da zero se il testo ha l'animazione specificata o zero in caso contrario.                                         |
| **\_Animazione dello stile del tipo di carattere TSATTRID \_ \_ \_ SHIMMER**            | Contiene un valore diverso da zero se il testo ha l'animazione specificata o zero in caso contrario.                                         |
| **\_Animazione dello stile del tipo di carattere TSATTRID \_ \_ \_ SparkleText**        | Contiene un valore diverso da zero se il testo ha l'animazione specificata o zero in caso contrario.                                         |
| **\_Animazione dello stile del tipo di carattere TSATTRID \_ \_ \_ WipeDown**           | Contiene un valore diverso da zero se il testo ha l'animazione specificata o zero in caso contrario.                                         |
| **\_Animazione dello stile del tipo di carattere TSATTRID \_ \_ \_ WipeRight**          | Contiene un valore diverso da zero se il testo ha l'animazione specificata o zero in caso contrario.                                         |
| **\_Stile del tipo di carattere TSATTRID \_ \_ BackgroundColor**               | Contiene il valore RGB dello sfondo del testo. Contiene 0xFF000000 se il colore del testo è automatico.                          |
| **\_Intermittenza stile del tipo di carattere TSATTRID \_ \_**                         | Contiene un valore diverso da zero se il testo è lampeggiante o zero in caso contrario.                                                         |
| **\_Stile del tipo di carattere TSATTRID \_ \_ grassetto**                          | Contiene un valore diverso da zero se il testo è in grassetto o zero in caso contrario.                                                             |
| **\_Stile carattere \_ TSATTRID \_ maiuscolo**                    | Contiene un valore diverso da zero se il testo è in maiuscolo o zero in caso contrario.                                                      |
| **\_ \_ Colore dello stile del tipo di carattere TSATTRID \_**                         | Contiene il valore RGB del colore del testo. Contiene 0xFF000000 se il colore del testo è automatico.                               |
| **\_ \_ Rilievo dello stile del tipo di carattere TSATTRID \_**                        | Contiene un valore diverso da zero se il testo è in rilievo o zero in caso contrario.                                                         |
| **TSATTRID \_ lo stile del tipo di carattere \_ \_**                       | Contiene un valore diverso da zero se il testo è inciso o zero in caso contrario.                                                         |
| **\_ \_ Altezza stile carattere \_ TSATTRID**                        | Contiene l'altezza del tipo di carattere. Per ulteriori informazioni, vedere il membro **lfHeight** della struttura LOGFONT.                       |
| **\_Stile del tipo di carattere TSATTRID \_ \_ nascosto**                        | Contiene un valore diverso da zero se il testo è nascosto o zero in caso contrario.                                                           |
| **\_Stile del tipo di carattere TSATTRID \_ \_ corsivo**                        | Contiene un valore diverso da zero se il testo è in corsivo o zero.                                                           |
| **\_ \_ Crenatura dello stile del tipo di carattere TSATTRID \_**                       | Contiene la dimensione minima della crenatura. Per altre informazioni, vedere ITextFont:: GetKerning.                                         |
| **TSATTRID \_ \_ stile carattere \_ minuscolo**                     | Contiene un valore diverso da zero se il testo è in minuscolo o zero.                                                        |
| **\_Stile del tipo di carattere TSATTRID \_ \_ illustrato**                      | Contiene un valore diverso da zero se il testo è delineato o zero in caso contrario.                                                         |
| **Linea di stile del tipo di \_ carattere TSATTRID \_ \_**                      | Contiene un valore diverso da zero se il testo viene sottolineato o zero in caso contrario.                                                        |
| **TSATTRID \_ di \_ stile del carattere \_ iperlinea \_ doppio**              | Contiene un valore diverso da zero se il testo è a doppio allineamento o zero in caso contrario.                                                 |
| **\_Riga di stile del tipo di carattere TSATTRID \_ \_ \_ Single**              | Contiene un valore diverso da zero se il testo è a singola riga o zero in caso contrario.                                                 |
| **\_ \_ Posizione dello stile del tipo di carattere TSATTRID \_**                      | Contiene la posizione del tipo di carattere.                                                                                                 |
| **\_Stile del tipo di carattere TSATTRID \_ \_ protetto**                     | Contiene un valore diverso da zero se il testo è protetto o zero in caso contrario.                                                        |
| **\_ \_ Ombreggiatura stile carattere TSATTRID \_**                        | Contiene un valore diverso da zero se il testo è ombreggiato o zero in caso contrario.                                                         |
| **\_SmallCaps stile del tipo di carattere TSATTRID \_ \_**                     | Contiene un valore diverso da zero se il testo è in minuscolo o zero.                                                        |
| **\_ \_ Spaziatura dello stile del tipo di carattere TSATTRID \_**                       | Contiene la spaziatura dei tipi di carattere.                                                                                                  |
| **\_Stile carattere \_ \_ barrato TSATTRID**                 | Non usato.                                                                                                                   |
| **\_Stile carattere \_ \_ BARRAto \_ doppio TSATTRID**         | Contiene un valore diverso da zero se il testo è doppio barrato o zero in caso contrario.                                             |
| **\_Stile carattere \_ \_ BARRAto \_ singolo TSATTRID**         | Contiene un valore diverso da zero se il testo è barrato singolo o zero in caso contrario.                                             |
| **\_ \_ Pedice dello stile del tipo di carattere TSATTRID \_**                     | Contiene un valore diverso da zero se il testo è pedice o zero in caso contrario.                                                        |
| **Apice dello stile del tipo di \_ carattere TSATTRID \_ \_**                   | Contiene un valore diverso da zero se il testo è apice o zero in caso contrario.                                                      |
| **\_Sottolineato stile del tipo di carattere TSATTRID \_ \_**                     | Contiene un valore diverso da zero se il testo è sottolineato o zero in caso contrario.                                                       |
| **TSATTRID \_ carattere \_ di \_ sottolineatura \_ doppio stile**             | Contiene un valore diverso da zero se il testo è doppio sottolineato o zero in caso contrario.                                                |
| **\_ \_ Sottolineatura TSATTRID stile carattere \_ \_ singolo**             | Contiene un valore diverso da zero se il testo è sottolineato o zero in caso contrario.                                                |
| **\_Stile carattere \_ TSATTRID \_ maiuscolo**                     | Contiene un valore diverso da zero se il testo è maiuscolo o zero in caso contrario.                                                        |
| **\_ \_ Spessore stile carattere \_ TSATTRID**                        | Contiene lo spessore del carattere. Per ulteriori informazioni sui valori possibili, vedere il membro **lfWeight** della struttura LOGFONT. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 


---
description: In questa sezione vengono descritte le strutture utilizzate con la \_ funzione Escape MXDC e Microsoft XPS Document Converter (MXDC).
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: Strutture di codice di escape MXDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b35c393d00dab227a91cbbb55eeca62039b41ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318361"
---
# <a name="mxdc-escape-code-structures"></a>Strutture di codice di escape MXDC

In questa sezione vengono descritte le strutture utilizzate con la [**funzione \_ escape MXDC**](mxdc-escape.md) e Microsoft XPS Document Converter (MXDC).

## <a name="in-this-section"></a>Contenuto della sezione



| Struttura                                                                              | Descrizione                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_intestazione di escape MXDC \_ \_ T**](mxdcescapeheader.md)<br/>                         | La struttura [**MXDC dell' \_ intestazione di escape \_ \_ T**](/windows/desktop/printdocs/mxdcescapeheader) include il codice operativo per una chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ escape**](mxdc-escape.md) come parametro *nEscape* . Fornisce anche le dimensioni dei buffer di input e di output.<br/>  |
| [**MXDC \_ ottenere \_ i dati del nome file \_ \_ T**](mxdcgetfilenamedata.md)<br/>                 | La struttura [**MXDC \_ get \_ filename \_ data \_ T**](/windows/desktop/printdocs/mxdcgetfilenamedata) include il percorso completo e il nome file di un file di output di Microsoft XPS Document Converter (MXDC).<br/>                                                                                                     |
| [**MXDC \_ di \_ escape PRINTTICKET \_ T**](mxdcprintticketescape.md)<br/>               | La struttura [**MXDC di \_ \_ escape PrintTicket \_ t**](mxdcprintticketescape.md) è una struttura di [**intestazione di escape MXDC \_ \_ \_ t**](mxdcescapeheader.md) concatenata a una struttura di [**\_ \_ data \_ t PrintTicket MXDC**](mxdcprintticketpassthrough.md) .<br/>                            |
| [**MXDC \_ \_ dati PRINTTICKET \_ T**](mxdcprintticketpassthrough.md)<br/>            | La struttura di [**\_ \_ data \_ T PRINTTICKET MXDC**](/windows/desktop/printdocs/mxdcprintticketpassthrough) contiene un ticket di stampa del documento XPS, che contiene le impostazioni della stampante e del processo di stampa, da passare al file di output Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.<br/>              |
| [**MXDC \_ S0PAGE \_ dati \_ T**](mxdcs0pagedata.md)<br/>                             | La struttura [**MXDC \_ S0PAGE \_ data \_ T**](/windows/desktop/printdocs/mxdcs0pagedata) include una pagina di documento XPS da passare al file di output di Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.<br/>                                                                                  |
| [**MXDC \_ S0PAGE \_ PassThrough \_ escape \_ T**](mxdcs0pagepassthroughescape.md)<br/> | La struttura [**MXDC \_ S0PAGE \_ PassThrough \_ escape \_ t**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape) è una struttura di [**\_ escape \_ \_ t MXDC**](mxdcescapeheader.md) concatenata a una struttura [**MXDC \_ S0PAGE \_ data \_ t**](mxdcs0pagedata.md) .<br/>                             |
| [**MXDC \_ S0PAGE \_ risorsa \_ escape \_ T**](mxdcs0pageresourceescape.md)<br/>       | La struttura [**MXDC \_ S0PAGE \_ Resource \_ escape \_ t**](/windows/desktop/printdocs/mxdcs0pageresourceescape) è una struttura di [**\_ escape \_ \_ t MXDC**](mxdcescapeheader.md) concatenata a una struttura della [**\_ \_ \_ risorsa \_ t S0PAGE XPS MXDC**](mxdcxpss0pageresource.md) .<br/>                   |
| [**\_Risorsa MXDC \_ XPS \_ S0PAGE \_ T**](mxdcxpss0pageresource.md)<br/>             | La struttura della [**\_ \_ \_ risorsa \_ T S0PAGE di MXDC XPS**](/windows/desktop/printdocs/mxdcxpss0pageresource) include informazioni su una risorsa, ad esempio un'immagine o un tipo di carattere, associato a una pagina del documento XPS e da passare al file di output di Microsoft XPS Document Converter (MXDC).<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_escape MXDC**](mxdc-escape.md)
</dt> </dl>

 


---
title: Informazioni sui controlli SysLink
description: Un controllo SysLink è una finestra che esegue il rendering del testo contrassegnato e invia una notifica all'applicazione quando gli utenti selezionano i collegamenti ipertestuali incorporati. Questo controllo rappresenta un'alternativa pratica all'uso del pulsante di collegamento Comando. Per altre informazioni, vedere Tipi di pulsante.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4a5d64af48fc0b48b15f22fff55e5cb563339ac8d90446981c74e07f5d4713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168561"
---
# <a name="about-syslink-controls"></a>Informazioni sui controlli SysLink

Un controllo SysLink è una finestra che esegue il rendering del testo contrassegnato e invia una notifica all'applicazione quando gli utenti selezionano i collegamenti ipertestuali incorporati. Questo controllo rappresenta un'alternativa pratica all'uso del [**pulsante di collegamento Comando**](button-styles.md). Per altre informazioni, vedere [Tipi di pulsante.](button-types-and-styles.md)

Ogni controllo SysLink può supportare più collegamenti ipertestuali ed è possibile accedere a ogni collegamento ipertestuale tramite un indice in base zero. Il controllo SysLink è definito nel ComCtl32.dll versione 6 e richiede un manifesto o una direttiva che specifica che deve essere usata la versione 6 della DLL, se disponibile. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

Questo articolo include le sezioni seguenti.

-   [SysLink Markup](#syslink-markup)
-   [Attributi di collegamento](#link-attributes)
-   [Stati dei collegamenti](#link-states)
-   [Limitazioni della visualizzazione di testo bidirezionale](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>SysLink Markup

Il controllo SysLink supporta il tag di ancoraggio ( &lt; a ) insieme agli attributi &gt; **HREF** e **ID**. Un **HREF** può essere qualsiasi protocollo, ad esempio http, ftp e mailto. Un **ID** è un nome facoltativo, univoco all'interno di un controllo SysLink, ed è associato a un singolo collegamento. Ai collegamenti viene inoltre assegnato un indice in base zero in base alla relativa posizione all'interno della stringa. Questo indice viene usato per accedere a un collegamento.

## <a name="link-attributes"></a>Attributi di collegamento

Gli attributi di ogni collegamento possono essere impostati all'interno del tag di ancoraggio per ogni collegamento o inviando il messaggio [**\_ LM SETITEM.**](lm-setitem.md) Se si imposta un attributo specificandolo all'interno della stringa di inizializzazione, il valore viene semplicemente inizializzato. È possibile modificare il valore di un attributo tramite l'uso successivo del messaggio **\_ LM SETITEM.**

## <a name="link-states"></a>Stati dei collegamenti

Gli elementi di collegamento possono essere in uno qualsiasi dei tre stati, rappresentati dai flag nella tabella seguente.



| Flag di stato   | Aspetto e significato                                            |
|--------------|-------------------------------------------------------------------|
| LIS \_ INCENTRATO | Il collegamento ha lo stato attivo e premendo INVIO viene attivato. |
| LIS \_ ABILITATO | Il collegamento è abilitato.                                              |
| LIS \_ VISITATO | L'utente ha già visitato l'URL rappresentato dal collegamento.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Limitazioni della visualizzazione di testo bidirezionale

Alcune lingue, ad esempio arabo o ebraico, sono scritte da destra a sinistra (RTL); L'inglese è scritto da sinistra a destra . La combinazione di RTL e LTR è detta testo bidirezionale. La combinazione di costrutti di markup direzionali Unicode o HTML LTR e RTL nelle stringhe di risorse, come marcatori di flusso bidirezionali per controllare il flusso delle stringhe, potrebbe non produrre il risultato previsto quando si usa un controllo SysLink. Ad esempio, una frase contrassegnata con LTR potrebbe non essere visualizzata correttamente nel contesto RTL.

> [!Note]  
> I controlli SysLink non supportano la visualizzazione bidirezionale in tutti gli scenari. Usare un controllo SysLink solo se si sa che un semplice layout LTR o RTL è adeguato. In caso contrario, è consigliabile usare una tecnologia più avanzata, ad [esempio MSHTML.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85))

 

 

 
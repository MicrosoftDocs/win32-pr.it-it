---
title: Informazioni sui controlli SysLink
description: Un controllo SysLink è una finestra che esegue il rendering del testo contrassegnato e invia una notifica all'applicazione quando gli utenti fanno clic sui collegamenti ipertestuali incorporati. Questo controllo offre una comoda alternativa all'uso del pulsante di collegamento al comando. Per altre informazioni, vedere tipi di pulsanti.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047425"
---
# <a name="about-syslink-controls"></a>Informazioni sui controlli SysLink

Un controllo SysLink è una finestra che esegue il rendering del testo contrassegnato e invia una notifica all'applicazione quando gli utenti fanno clic sui collegamenti ipertestuali incorporati. Questo controllo offre una comoda alternativa all'uso del [**pulsante di collegamento al comando**](button-styles.md). Per altre informazioni, vedere [tipi di pulsanti](button-types-and-styles.md).

Ogni controllo SysLink può supportare più collegamenti ipertestuali ed è possibile accedere a ogni collegamento ipertestuale tramite un indice in base zero. Il controllo SysLink è definito nel ComCtl32.dll versione 6 ed è necessario un manifesto o una direttiva che specifichi che la versione 6 della DLL deve essere utilizzata se disponibile. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

Questo articolo include le sezioni seguenti.

-   [Markup SysLink](#syslink-markup)
-   [Attributi di collegamento](#link-attributes)
-   [Stati di collegamento](#link-states)
-   [Limitazioni sulla visualizzazione del testo bidirezionale](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>Markup SysLink

Il controllo SysLink supporta il tag di ancoraggio ( &lt; a &gt; ) insieme agli attributi **href** e **ID**. Un **href** può essere qualsiasi protocollo, ad esempio http, FTP e mailto. Un **ID** è un nome facoltativo, univoco all'interno di un controllo Syslink, ed è associato a un singolo collegamento. Ai collegamenti viene inoltre assegnato un indice in base zero in base alla relativa posizione all'interno della stringa. Questo indice viene utilizzato per accedere a un collegamento.

## <a name="link-attributes"></a>Attributi di collegamento

È possibile impostare gli attributi di ogni collegamento all'interno del tag di ancoraggio per ogni collegamento o inviando il messaggio di [**\_ elemento**](lm-setitem.md) . Se si imposta un attributo specificandone il valore all'interno della stringa di inizializzazione, viene semplicemente inizializzato. È possibile modificare il valore di un attributo tramite l'uso successivo del messaggio di **\_ elemento** .

## <a name="link-states"></a>Stati di collegamento

Gli elementi del collegamento possono trovarsi in uno dei tre stati, rappresentati dai flag nella tabella seguente.



| Flag di stato   | Aspetto e significato                                            |
|--------------|-------------------------------------------------------------------|
| LIS con stato \_ attivo | Il collegamento ha lo stato attivo della tastiera e premendo invio lo attiva. |
| LIS \_ abilitato | Il collegamento è abilitato.                                              |
| LIS \_ visitato | L'utente ha già visitato l'URL rappresentato dal collegamento.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Limitazioni sulla visualizzazione del testo bidirezionale

Alcuni linguaggi, come l'arabo o l'ebraico, sono scritti da destra a sinistra (RTL); L'inglese è scritto da sinistra a destra (LTR). La combinazione di RTL con LTR viene chiamata testo bidirezionale. La combinazione di costrutti di markup direzionali LTR e RTL Unicode o HTML in stringhe di risorsa, come marcatori di flusso bidirezionali per controllare il flusso di stringhe, potrebbe non produrre il risultato previsto quando si usa un controllo SysLink. Ad esempio, una frase con contrassegno LTR potrebbe non essere visualizzata correttamente nel contesto di RTL.

> [!Note]  
> I controlli SysLink non supportano la visualizzazione bidirezionale in tutti gli scenari. Usare un controllo SysLink solo se si è certi che un semplice layout di LTR o RTL è sufficiente. In caso contrario, prendere in considerazione l'utilizzo di una tecnologia più avanzata, ad esempio [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).

 

 

 
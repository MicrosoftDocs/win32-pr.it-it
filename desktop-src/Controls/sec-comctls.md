---
title: Considerazioni sulla sicurezza controlli Microsoft Windows
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate ai controlli Windows.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104118610"
---
# <a name="security-considerations-microsoft-windows-controls"></a>Considerazioni sulla sicurezza: controlli di Microsoft Windows

In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate ai controlli Windows. Le informazioni contenute in questo argomento non forniscono tutto ciò che è necessario sapere sui problemi di sicurezza. è possibile utilizzarlo come punto di partenza e riferimento per questa area tecnologica.

L'interconnettività tra computer è comune; la preoccupazione principale di uno sviluppatore deve essere la sicurezza dell'applicazione. Le sezioni seguenti illustrano alcuni potenziali problemi di sicurezza da prendere in considerazione durante la programmazione dei controlli Windows.

-   [Messaggi di controllo con terminazione null](#null-terminated-control-messages)
-   [Utilizzo stringa](#string-use)
-   [Convalida dell'input](#input-validation)
-   [Uso della password](#password-use)
-   [Avvisi di sicurezza](#security-alerts)
-   [Argomenti correlati](#related-topics)

## <a name="null-terminated-control-messages"></a>Messaggi di controllo con terminazione null

Molti dei messaggi di controllo e delle macro hanno parametri di stringa. Spesso questi messaggi non convalidano le stringhe di input, in particolare, non verificano la presenza di un'interruzione `'\0'` . Quando si chiama un messaggio che usa una stringa come parametro, specificare in modo esplicito che la stringa è con terminazione null.

## <a name="string-use"></a>Utilizzo stringa

Quando si programmano i controlli di Windows, è necessario modificare le stringhe. Quasi tutti i controlli richiedono il testo da inserire. Per popolare una casella di riepilogo, ad esempio, è necessario caricare le stringhe nel controllo. Poiché l'uso errato delle stringhe causa spesso sovraccarichi del buffer, adottare le precauzioni per evitare questo rischio per la sicurezza.

Per altre informazioni sui sovraccarichi del buffer, vedere *scrittura di codice sicuro* da Michael Howard e David LeBlanc, Microsoft Press, 2002 e [procedure consigliate per le API di sicurezza](/windows/desktop/SecBP/best-practices-for-the-security-apis).

## <a name="input-validation"></a>Convalida dell'input

I messaggi di controllo seguenti possono presentare problemi di sicurezza.

-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**\_GETISEARCHSTRING LVM**](lvm-getisearchstring.md)
-   [**SB \_ GETtext**](sb-gettext.md)
-   [**\_GETTIPTEXT SB**](sb-gettiptext.md)
-   [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
-   [**GetText TTM \_**](ttm-gettext.md)
-   [**\_GETISEARCHSTRING TVM**](tvm-getisearchstring.md)

Se il testo viene modificato tra la chiamata per ottenere la lunghezza del testo e l'ora di visualizzazione o di utilizzo del testo, può verificarsi un sovraccarico del buffer. Per evitare questo problema, è necessario convalidare la stringa prima di utilizzarla. Inoltre, i messaggi che recuperano testo, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)e [**TTM \_ gettext**](ttm-gettext.md), non hanno un parametro di dimensione del buffer che presenta il potenziale per un sovraccarico del buffer.

Quando si usa [**CB \_ GETLBTEXT**](cb-getlbtext.md) o [**SB \_ gettext**](sb-gettext.md), è necessario chiamare prima [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) o [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere la dimensione del buffer. Alcuni di questi messaggi, [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)e [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md), possono essere chiamati con un valore di parametro **null** per ottenere la lunghezza della stringa prima di richiamare il messaggio per recuperare la stringa.

Un messaggio a cui è necessario prestare particolare attenzione è il messaggio [**\_ GETTIPTEXT**](sb-gettiptext.md) della barra di stato. Questo messaggio non fornisce alcun modo per eseguire una query sulla lunghezza della stringa da recuperare.

## <a name="password-use"></a>Uso della password

Se si usano i controlli di modifica protetti da password (stile di [**\_ password es**](edit-control-styles.md) ), il buffer che contiene il testo recuperato deve essere impostato su zero il prima possibile per evitare di esporre la password dell'utente in memoria.

## <a name="security-alerts"></a>Avvisi di sicurezza

Nella tabella seguente sono elencate le funzionalità che, se usate in modo non corretto, possono compromettere la sicurezza delle applicazioni. I messaggi elencati di seguito non forniscono un parametro che specifica le dimensioni del buffer.



| Funzionalità                                               | Strategia di riduzione del rischio                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | Verificare che sia possibile scrivere nel buffer usato dalla funzione e che sia a terminazione null.                                                                     |
| [**CB \_ GETLBTEXT**](cb-getlbtext.md)                 | Chiamare [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) per ottenere la dimensione del buffer e quindi chiamare [**CB \_ GETLBTEXT**](cb-getlbtext.md) per recuperare la stringa. |
| [**\_GETISEARCHSTRING LVM**](lvm-getisearchstring.md) | Chiamare il messaggio con un valore di parametro **null** per ottenere la dimensione del buffer, quindi chiamare il messaggio una seconda volta per recuperare la stringa.             |
| [**SB \_ GETtext**](sb-gettext.md)                     | Chiamare [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere la dimensione del buffer, quindi chiamare [**SB \_ gettext**](sb-gettext.md) per recuperare la stringa.   |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)         | Chiamare il messaggio con un valore di parametro **null** per ottenere la dimensione del buffer, quindi chiamare il messaggio una seconda volta per recuperare la stringa.             |
| [**GetText TTM \_**](ttm-gettext.md)                   | Questo messaggio non fornisce un modo per stabilire o specificare le dimensioni del buffer.                                                                  |
| [**\_GETISEARCHSTRING TVM**](tvm-getisearchstring.md) | Chiamare il messaggio passando un valore di parametro **null** per ottenere la dimensione del buffer, quindi chiamare il messaggio una seconda volta per recuperare la stringa.       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Altre risorse**
</dt> <dt>

[Microsoft Security](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Sicurezza](/windows/desktop/security)
</dt> <dt>

[Risorse di sicurezza TechNet](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[Procedure consigliate per le API di sicurezza](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 
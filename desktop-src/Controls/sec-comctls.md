---
title: Considerazioni sulla sicurezza per i controlli Windows Microsoft
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate ai controlli Windows personalizzati.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45faa0f3d2f521038c056055329d70541625bac88c16e62c1581b55ae2a6c5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696511"
---
# <a name="security-considerations-microsoft-windows-controls"></a>Considerazioni sulla sicurezza: Controlli Windows Microsoft

In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate ai controlli Windows personalizzati. Le informazioni contenute in questo argomento non forniscono tutte le informazioni necessarie sui problemi di sicurezza: usarle come punto di partenza e riferimento per questa area di tecnologia.

L'interconnettività tra computer è comune; Il problema principale di uno sviluppatore deve essere la sicurezza delle applicazioni. Le sezioni seguenti illustrano alcuni potenziali problemi di sicurezza da considerare durante la programmazione Windows controlli .

-   [Messaggi di controllo con terminazione Null](#null-terminated-control-messages)
-   [Uso delle stringhe](#string-use)
-   [Convalida dell'input](#input-validation)
-   [Uso della password](#password-use)
-   [Avvisi di sicurezza](#security-alerts)
-   [Argomenti correlati](#related-topics)

## <a name="null-terminated-control-messages"></a>Messaggi di controllo con terminazione Null

Molti dei messaggi di controllo e delle macro hanno parametri di stringa. Spesso questi messaggi non convalidano le stringhe di input, in particolare non verificano la presenza di un oggetto di `'\0'` terminazione. Quando si chiama un messaggio che usa una stringa come parametro, specificare in modo esplicito che la stringa ha terminazione Null.

## <a name="string-use"></a>Uso delle stringhe

Quando si programmano Windows controlli, è necessario modificare le stringhe. Quasi tutti i controlli richiedono l'inserimento di testo. Ad esempio, per popolare una casella di riepilogo è necessario caricare stringhe nel controllo . Poiché l'uso errato delle stringhe causa spesso sovraccarichi del buffer, adottare precauzioni per evitare questo rischio per la sicurezza.

Per altre informazioni sui sovraccarichi del buffer, vedere Writing *Secure Code* (Scrittura di codice sicuro) di Michael Michael Michael e David LeBlanc, Microsoft Press, 2002 e Best Practices for the [Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis)(Procedure consigliate per le API di sicurezza).

## <a name="input-validation"></a>Convalida dell'input

I messaggi di controllo seguenti possono presentare problemi di sicurezza.

-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)
-   [**SB \_ GETTEXT**](sb-gettext.md)
-   [**SB \_ GETTIPTEXT**](sb-gettiptext.md)
-   [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
-   [**TTM \_ GETTEXT**](ttm-gettext.md)
-   [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)

Se il testo cambia tra la chiamata per ottenere la lunghezza del testo e l'ora in cui il testo viene visualizzato o usato, può verificarsi un sovraccarico del buffer. Per evitare questo problema, è necessario convalidare la stringa prima di usarla. Inoltre, i messaggi che recuperano testo, [**CB \_ GETLBTEXT,**](cb-getlbtext.md) [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)e [**TTM \_ GETTEXT,**](ttm-gettext.md)non hanno alcun parametro di dimensione del buffer che presenta la possibilità di un sovraccarico del buffer.

Quando si usa [**CB \_ GETLBTEXT**](cb-getlbtext.md) o [**SB \_ GETTEXT,**](sb-gettext.md)è prima necessario chiamare [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) o [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere le dimensioni del buffer. Alcuni di questi messaggi, [**TB \_ GETBUTTONTEXT,**](tb-getbuttontext.md) [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)e [**TVM \_ GETISEARCHSTRING,**](tvm-getisearchstring.md)possono essere chiamati con un valore di parametro **NULL** per ottenere la lunghezza della stringa prima di richiamare il messaggio per recuperare la stringa.

Un messaggio a cui è necessario prestare particolare attenzione è il messaggio [**SB \_ GETTIPTEXT della barra**](sb-gettiptext.md) di stato. Questo messaggio non consente di eseguire query sulla lunghezza della stringa da recuperare.

## <a name="password-use"></a>Uso della password

Se si usano controlli di modifica protetti da password (stile [**ES \_ PASSWORD),**](edit-control-styles.md) il buffer che contiene il testo recuperato deve essere impostato su zero appena possibile per evitare di esporre la password dell'utente in memoria.

## <a name="security-alerts"></a>Avvisi di sicurezza

Nella tabella seguente sono elencate le funzionalità che, se usate in modo non corretto, possono compromettere la sicurezza delle applicazioni. I messaggi elencati di seguito non forniscono un parametro che specifica le dimensioni del buffer.



| Funzionalità                                               | Strategia di riduzione del rischio                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | Assicurarsi che il buffer usato dalla funzione possa essere scritto in e con terminazione Null.                                                                     |
| [**CB \_ GETLBTEXT**](cb-getlbtext.md)                 | Chiamare [**CB \_ GETLBTEXTLEN per**](cb-getlbtextlen.md) ottenere le dimensioni del buffer e quindi chiamare [**CB \_ GETLBTEXT**](cb-getlbtext.md) per recuperare la stringa. |
| [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md) | Chiamare il messaggio con un **valore di** parametro NULL per ottenere le dimensioni del buffer e quindi chiamare il messaggio una seconda volta per recuperare la stringa.             |
| [**SB \_ GETTEXT**](sb-gettext.md)                     | Chiamare [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere le dimensioni del buffer, quindi [**chiamare SB \_ GETTEXT**](sb-gettext.md) per recuperare la stringa.   |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)         | Chiamare il messaggio con un **valore di** parametro NULL per ottenere le dimensioni del buffer e quindi chiamare il messaggio una seconda volta per recuperare la stringa.             |
| [**TTM \_ GETTEXT**](ttm-gettext.md)                   | Questo messaggio non consente di conoscere o specificare le dimensioni del buffer.                                                                  |
| [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md) | Chiamare il messaggio passando un **valore di parametro NULL** per ottenere le dimensioni del buffer, quindi chiamare il messaggio una seconda volta per recuperare la stringa.       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Altre risorse**
</dt> <dt>

[Microsoft Security](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Sicurezza](/windows/desktop/security)
</dt> <dt>

[Risorse per la sicurezza di TechNet](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[Procedure consigliate per le API di sicurezza](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 
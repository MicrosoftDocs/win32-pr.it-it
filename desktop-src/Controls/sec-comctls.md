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
# <a name="security-considerations-microsoft-windows-controls"></a><span data-ttu-id="212cd-103">Considerazioni sulla sicurezza: controlli di Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="212cd-103">Security Considerations: Microsoft Windows Controls</span></span>

<span data-ttu-id="212cd-104">In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate ai controlli Windows.</span><span class="sxs-lookup"><span data-stu-id="212cd-104">This topic provides information about security considerations related to the Windows controls.</span></span> <span data-ttu-id="212cd-105">Le informazioni contenute in questo argomento non forniscono tutto ciò che è necessario sapere sui problemi di sicurezza. è possibile utilizzarlo come punto di partenza e riferimento per questa area tecnologica.</span><span class="sxs-lookup"><span data-stu-id="212cd-105">The information in this topic does not provide all you need to know about security issues—use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="212cd-106">L'interconnettività tra computer è comune; la preoccupazione principale di uno sviluppatore deve essere la sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="212cd-106">Interconnectivity among computers is common; a developer's chief concern must be application security.</span></span> <span data-ttu-id="212cd-107">Le sezioni seguenti illustrano alcuni potenziali problemi di sicurezza da prendere in considerazione durante la programmazione dei controlli Windows.</span><span class="sxs-lookup"><span data-stu-id="212cd-107">The following sections discuss some potential security issues to consider when programming Windows controls.</span></span>

-   [<span data-ttu-id="212cd-108">Messaggi di controllo con terminazione null</span><span class="sxs-lookup"><span data-stu-id="212cd-108">Null-terminated Control Messages</span></span>](#null-terminated-control-messages)
-   [<span data-ttu-id="212cd-109">Utilizzo stringa</span><span class="sxs-lookup"><span data-stu-id="212cd-109">String Use</span></span>](#string-use)
-   [<span data-ttu-id="212cd-110">Convalida dell'input</span><span class="sxs-lookup"><span data-stu-id="212cd-110">Input Validation</span></span>](#input-validation)
-   [<span data-ttu-id="212cd-111">Uso della password</span><span class="sxs-lookup"><span data-stu-id="212cd-111">Password Use</span></span>](#password-use)
-   [<span data-ttu-id="212cd-112">Avvisi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="212cd-112">Security Alerts</span></span>](#security-alerts)
-   [<span data-ttu-id="212cd-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="212cd-113">Related topics</span></span>](#related-topics)

## <a name="null-terminated-control-messages"></a><span data-ttu-id="212cd-114">Messaggi di controllo con terminazione null</span><span class="sxs-lookup"><span data-stu-id="212cd-114">Null-terminated Control Messages</span></span>

<span data-ttu-id="212cd-115">Molti dei messaggi di controllo e delle macro hanno parametri di stringa.</span><span class="sxs-lookup"><span data-stu-id="212cd-115">Many of the control messages and macros have string parameters.</span></span> <span data-ttu-id="212cd-116">Spesso questi messaggi non convalidano le stringhe di input, in particolare, non verificano la presenza di un'interruzione `'\0'` .</span><span class="sxs-lookup"><span data-stu-id="212cd-116">Often these messages do not validate the input strings, in particular, they do not check for a terminating `'\0'`.</span></span> <span data-ttu-id="212cd-117">Quando si chiama un messaggio che usa una stringa come parametro, specificare in modo esplicito che la stringa è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="212cd-117">When you call a message that uses a string as a parameter, explicitly specify that the string is null-terminated.</span></span>

## <a name="string-use"></a><span data-ttu-id="212cd-118">Utilizzo stringa</span><span class="sxs-lookup"><span data-stu-id="212cd-118">String Use</span></span>

<span data-ttu-id="212cd-119">Quando si programmano i controlli di Windows, è necessario modificare le stringhe.</span><span class="sxs-lookup"><span data-stu-id="212cd-119">When you program Windows controls, it is necessary to manipulate strings.</span></span> <span data-ttu-id="212cd-120">Quasi tutti i controlli richiedono il testo da inserire.</span><span class="sxs-lookup"><span data-stu-id="212cd-120">Almost every control requires text to be inserted.</span></span> <span data-ttu-id="212cd-121">Per popolare una casella di riepilogo, ad esempio, è necessario caricare le stringhe nel controllo.</span><span class="sxs-lookup"><span data-stu-id="212cd-121">For example, to populate a list box you must load strings into the control.</span></span> <span data-ttu-id="212cd-122">Poiché l'uso errato delle stringhe causa spesso sovraccarichi del buffer, adottare le precauzioni per evitare questo rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="212cd-122">Because using strings incorrectly often causes buffer overruns, take precautions to avoid this security risk.</span></span>

<span data-ttu-id="212cd-123">Per altre informazioni sui sovraccarichi del buffer, vedere *scrittura di codice sicuro* da Michael Howard e David LeBlanc, Microsoft Press, 2002 e [procedure consigliate per le API di sicurezza](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="212cd-123">For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span>

## <a name="input-validation"></a><span data-ttu-id="212cd-124">Convalida dell'input</span><span class="sxs-lookup"><span data-stu-id="212cd-124">Input Validation</span></span>

<span data-ttu-id="212cd-125">I messaggi di controllo seguenti possono presentare problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="212cd-125">The following control messages can present security problems.</span></span>

-   [<span data-ttu-id="212cd-126">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="212cd-126">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
-   [<span data-ttu-id="212cd-127">**\_GETISEARCHSTRING LVM**</span><span class="sxs-lookup"><span data-stu-id="212cd-127">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md)
-   [<span data-ttu-id="212cd-128">**SB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="212cd-128">**SB\_GETTEXT**</span></span>](sb-gettext.md)
-   [<span data-ttu-id="212cd-129">**\_GETTIPTEXT SB**</span><span class="sxs-lookup"><span data-stu-id="212cd-129">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)
-   [<span data-ttu-id="212cd-130">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="212cd-130">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
-   [<span data-ttu-id="212cd-131">**GetText TTM \_**</span><span class="sxs-lookup"><span data-stu-id="212cd-131">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)
-   [<span data-ttu-id="212cd-132">**\_GETISEARCHSTRING TVM**</span><span class="sxs-lookup"><span data-stu-id="212cd-132">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md)

<span data-ttu-id="212cd-133">Se il testo viene modificato tra la chiamata per ottenere la lunghezza del testo e l'ora di visualizzazione o di utilizzo del testo, può verificarsi un sovraccarico del buffer.</span><span class="sxs-lookup"><span data-stu-id="212cd-133">If the text changes between the call to get the text length and the time the text is displayed or used, a buffer overrun can occur.</span></span> <span data-ttu-id="212cd-134">Per evitare questo problema, è necessario convalidare la stringa prima di utilizzarla.</span><span class="sxs-lookup"><span data-stu-id="212cd-134">To avoid this, you must validate the string before using it.</span></span> <span data-ttu-id="212cd-135">Inoltre, i messaggi che recuperano testo, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)e [**TTM \_ gettext**](ttm-gettext.md), non hanno un parametro di dimensione del buffer che presenta il potenziale per un sovraccarico del buffer.</span><span class="sxs-lookup"><span data-stu-id="212cd-135">In addition, the messages that retrieve text, [**CB\_GETLBTEXT**](cb-getlbtext.md), [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), and [**TTM\_GETTEXT**](ttm-gettext.md), have no buffer size parameter that presents the potential for a buffer overrun.</span></span>

<span data-ttu-id="212cd-136">Quando si usa [**CB \_ GETLBTEXT**](cb-getlbtext.md) o [**SB \_ gettext**](sb-gettext.md), è necessario chiamare prima [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) o [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="212cd-136">When you use [**CB\_GETLBTEXT**](cb-getlbtext.md) or [**SB\_GETTEXT**](sb-gettext.md), you should first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) or [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size.</span></span> <span data-ttu-id="212cd-137">Alcuni di questi messaggi, [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)e [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md), possono essere chiamati con un valore di parametro **null** per ottenere la lunghezza della stringa prima di richiamare il messaggio per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="212cd-137">Some of these messages, [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM\_GETISEARCHSTRING**](lvm-getisearchstring.md), and [**TVM\_GETISEARCHSTRING**](tvm-getisearchstring.md), can be called with a **NULL** parameter value to obtain the length of the string before invoking the message to retrieve the string.</span></span>

<span data-ttu-id="212cd-138">Un messaggio a cui è necessario prestare particolare attenzione è il messaggio [**\_ GETTIPTEXT**](sb-gettiptext.md) della barra di stato.</span><span class="sxs-lookup"><span data-stu-id="212cd-138">A message that you should pay particular attention to is the status bar [**SB\_GETTIPTEXT**](sb-gettiptext.md) message.</span></span> <span data-ttu-id="212cd-139">Questo messaggio non fornisce alcun modo per eseguire una query sulla lunghezza della stringa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="212cd-139">This message provides no way to query the length of the string that is to be retrieved.</span></span>

## <a name="password-use"></a><span data-ttu-id="212cd-140">Uso della password</span><span class="sxs-lookup"><span data-stu-id="212cd-140">Password Use</span></span>

<span data-ttu-id="212cd-141">Se si usano i controlli di modifica protetti da password (stile di [**\_ password es**](edit-control-styles.md) ), il buffer che contiene il testo recuperato deve essere impostato su zero il prima possibile per evitare di esporre la password dell'utente in memoria.</span><span class="sxs-lookup"><span data-stu-id="212cd-141">If you use password-protected edit controls ([**ES\_PASSWORD**](edit-control-styles.md) style), the buffer that contains the retrieved text must be set to zero as soon as possible to avoid exposing the user's password in memory.</span></span>

## <a name="security-alerts"></a><span data-ttu-id="212cd-142">Avvisi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="212cd-142">Security Alerts</span></span>

<span data-ttu-id="212cd-143">Nella tabella seguente sono elencate le funzionalità che, se usate in modo non corretto, possono compromettere la sicurezza delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="212cd-143">The following table lists features that, if used incorrectly, can compromise the security of your applications.</span></span> <span data-ttu-id="212cd-144">I messaggi elencati di seguito non forniscono un parametro che specifica le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="212cd-144">The messages listed here do not provide a parameter that specifies the buffer size.</span></span>



| <span data-ttu-id="212cd-145">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="212cd-145">Feature</span></span>                                               | <span data-ttu-id="212cd-146">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="212cd-146">Mitigation</span></span>                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="212cd-147">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="212cd-147">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | <span data-ttu-id="212cd-148">Verificare che sia possibile scrivere nel buffer usato dalla funzione e che sia a terminazione null.</span><span class="sxs-lookup"><span data-stu-id="212cd-148">Make sure the buffer used by the function can be written to and is null-terminated.</span></span>                                                                     |
| [<span data-ttu-id="212cd-149">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="212cd-149">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)                 | <span data-ttu-id="212cd-150">Chiamare [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) per ottenere la dimensione del buffer e quindi chiamare [**CB \_ GETLBTEXT**](cb-getlbtext.md) per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="212cd-150">Call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to obtain the buffer size, and then call [**CB\_GETLBTEXT**](cb-getlbtext.md) to retrieve the string.</span></span> |
| [<span data-ttu-id="212cd-151">**\_GETISEARCHSTRING LVM**</span><span class="sxs-lookup"><span data-stu-id="212cd-151">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md) | <span data-ttu-id="212cd-152">Chiamare il messaggio con un valore di parametro **null** per ottenere la dimensione del buffer, quindi chiamare il messaggio una seconda volta per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="212cd-152">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="212cd-153">**SB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="212cd-153">**SB\_GETTEXT**</span></span>](sb-gettext.md)                     | <span data-ttu-id="212cd-154">Chiamare [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere la dimensione del buffer, quindi chiamare [**SB \_ gettext**](sb-gettext.md) per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="212cd-154">Call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size, and then call [**SB\_GETTEXT**](sb-gettext.md) to retrieve the string.</span></span>   |
| [<span data-ttu-id="212cd-155">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="212cd-155">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)         | <span data-ttu-id="212cd-156">Chiamare il messaggio con un valore di parametro **null** per ottenere la dimensione del buffer, quindi chiamare il messaggio una seconda volta per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="212cd-156">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="212cd-157">**GetText TTM \_**</span><span class="sxs-lookup"><span data-stu-id="212cd-157">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)                   | <span data-ttu-id="212cd-158">Questo messaggio non fornisce un modo per stabilire o specificare le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="212cd-158">This message does not provide a way for you to know or specify the size of the buffer.</span></span>                                                                  |
| [<span data-ttu-id="212cd-159">**\_GETISEARCHSTRING TVM**</span><span class="sxs-lookup"><span data-stu-id="212cd-159">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md) | <span data-ttu-id="212cd-160">Chiamare il messaggio passando un valore di parametro **null** per ottenere la dimensione del buffer, quindi chiamare il messaggio una seconda volta per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="212cd-160">Call the message by passing a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="212cd-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="212cd-161">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="212cd-162">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="212cd-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="212cd-163">Microsoft Security</span><span class="sxs-lookup"><span data-stu-id="212cd-163">Microsoft Security</span></span>](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[<span data-ttu-id="212cd-164">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="212cd-164">Security</span></span>](/windows/desktop/security)
</dt> <dt>

[<span data-ttu-id="212cd-165">Risorse di sicurezza TechNet</span><span class="sxs-lookup"><span data-stu-id="212cd-165">TechNet Security Resources</span></span>](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[<span data-ttu-id="212cd-166">Procedure consigliate per le API di sicurezza</span><span class="sxs-lookup"><span data-stu-id="212cd-166">Best Practices for the Security APIs</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 
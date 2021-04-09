---
title: Corpo ACF
description: Il corpo di ACF contiene gli attributi di configurazione che si applicano ai tipi e alle funzioni definiti nel corpo dell'interfaccia del file IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104047509"
---
# <a name="the-acf-body"></a>Corpo ACF

Il corpo di ACF contiene gli attributi di configurazione che si applicano ai tipi e alle funzioni definiti nel corpo dell'interfaccia del file IDL. Il corpo di ACF può essere vuoto o contenere gli attributi di [**inclusione**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), funzione e parametro di ACF. Tutti questi elementi sono facoltativi. Attributi applicati a singoli tipi e funzioni nel corpo di ACF che eseguono l'override degli attributi nell'intestazione ACF.

L'ACF specifica il comportamento nel computer locale e non influisce sui dati trasmessi in rete. Viene utilizzato per specificare i dettagli di uno stub da generare. In modalità di compatibilità DCE ([**/OSF**](/windows/desktop/Midl/-osf)), ACF non influisce sull'interazione tra gli stub, ma tra lo stub e il codice dell'applicazione.

Un parametro specificato in ACF deve essere uno dei parametri specificati nel file IDL. L'ordine di specifica del parametro nell'elemento ACF non è significativo perché la corrispondenza è in base al nome, non in base alla posizione. L'elenco di parametri in ACF può essere vuoto, anche quando l'elenco dei parametri nella firma IDL corrispondente non è (ma questa operazione non è consigliata). I dichiaratori astratti (parametri senza nome) nel file IDL fanno sì che il compilatore MIDL segnali errori durante l'elaborazione di ACF perché il parametro non è stato trovato.

La direttiva di **inclusione** di ACF specifica i file di intestazione da visualizzare nell'intestazione generata come parte di un'istruzione di **\# inclusione** del preprocessore C standard. La parola chiave ACF **include** differisce da una direttiva **\# include** . La parola chiave ACF **include** fa in modo che la riga "**\# Includi** *filename*" venga visualizzata nel file di intestazione generato, mentre la direttiva del linguaggio C "**\# include** *filename*" fa sì che il contenuto del file venga inserito nell'ACF.

L'istruzione ACF [**typedef**](/windows/desktop/Midl/typedef) consente di applicare gli attributi di tipo ACF ai tipi definiti in precedenza nel file IDL. La sintassi di ACF **typedef** è diversa dalla sintassi del **typedef** C.

Gli attributi della funzione ACF consentono di specificare gli attributi che si applicano alla funzione nel suo complesso. Per ulteriori informazioni, vedere **\[** [**Code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimize**](/windows/desktop/Midl/optimize) **\]** e **\[** [**NoCode**](/windows/desktop/Midl/nocode) **\]** .

Gli attributi del parametro ACF consentono di specificare gli attributi che si applicano ai singoli parametri della funzione. Per ulteriori informazioni, vedere **\[** [**\_ conteggio byte**](/windows/desktop/Midl/byte-count) **\]** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**configurazione di/app \_**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[\_handle automatico\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[codice\]**](../midl/code.md)
</dt> <dt>

[**\[handle esplicito \_\]**](../midl/explicit-handle.md)
</dt> <dt>

[File IDL (Interface Definition Language)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[handle implicito \_\]**](../midl/implicit-handle.md)
</dt> <dt>

[**includere**](/windows/desktop/Midl/include)
</dt> <dt>

[MIDL](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[NoCode\]**](../midl/nocode.md)
</dt> <dt>

[**\[ottimizzare\]**](../midl/optimize.md)
</dt> <dt>

[**\[rappresenta \_ come\]**](../midl/represent-as.md)
</dt> <dt>

[**typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 
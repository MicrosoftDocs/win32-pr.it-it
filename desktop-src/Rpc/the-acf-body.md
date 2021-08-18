---
title: Corpo di ACF
description: Il corpo di ACF contiene gli attributi di configurazione che si applicano ai tipi e alle funzioni definiti nel corpo dell'interfaccia del file IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1446b4f0e14849832766bc512a95d0ae0aeb249cebd814314b617ffa1e1125e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924621"
---
# <a name="the-acf-body"></a>Corpo di ACF

Il corpo di ACF contiene gli attributi di configurazione che si applicano ai tipi e alle funzioni definiti nel corpo dell'interfaccia del file IDL. Il corpo di ACF può essere vuoto o può contenere gli attributi [**ACF,**](/windows/desktop/Midl/include) [**typedef,**](/windows/desktop/Midl/typedef)function e parameter. Tutti questi elementi sono facoltativi. Gli attributi applicati a singoli tipi e funzioni nel corpo ACF eseguono l'override degli attributi nell'intestazione ACF.

L'ACF specifica il comportamento nel computer locale e non influisce sui dati trasmessi in rete. Viene usato per specificare i dettagli di uno stub da generare. In modalità di compatibilità DCE ([**/osf**](/windows/desktop/Midl/-osf)), ACF non influisce sull'interazione tra stub, ma tra lo stub e il codice dell'applicazione.

Un parametro specificato in ACF deve essere uno dei parametri specificati nel file IDL. L'ordine di specifica del parametro in ACF non è significativo perché la corrispondenza è in base al nome, non alla posizione. L'elenco di parametri in ACF può essere vuoto, anche quando l'elenco di parametri nella firma IDL corrispondente non è (ma questa operazione non è consigliata). I dichiaratori astratti (parametri senza nome) nel file IDL causano errori del compilatore MIDL durante l'elaborazione di ACF perché il parametro non viene trovato.

La direttiva **include** acf specifica i file di intestazione da visualizzare nell'intestazione generata come parte di un'istruzione include del **\# preprocessore** C standard. La parola chiave ACF **include** è diversa da una **\# direttiva include.** La parola chiave **ACF include** fa sì che la riga "**\# include** *filename*" venga visualizzata nel file di intestazione generato, mentre la direttiva del linguaggio C "**\# include** *filename*" fa sì che il contenuto del file venga inserito nel file ACF.

L'istruzione [**typedef**](/windows/desktop/Midl/typedef) ACF consente di applicare attributi di tipo ACF ai tipi definiti in precedenza nel file IDL. La sintassi **del typedef** ACF è diversa dalla sintassi **typedef** C.

Gli attributi della funzione ACF consentono di specificare gli attributi applicabili all'intera funzione. Per altre informazioni, vedere **\[** [**code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimize**](/windows/desktop/Midl/optimize) **\]** e **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** .

Gli attributi dei parametri ACF consentono di specificare gli attributi applicabili ai singoli parametri della funzione. Per altre informazioni, vedere **\[** [**Numero di \_**](/windows/desktop/Midl/byte-count) **\]** byte.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**/app \_ config**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[handle \_ automatico\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[Codice\]**](../midl/code.md)
</dt> <dt>

[**\[handle \_ esplicito\]**](../midl/explicit-handle.md)
</dt> <dt>

[File IDL (Interface Definition Language)](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[handle \_ implicito\]**](../midl/implicit-handle.md)
</dt> <dt>

[**Includono**](/windows/desktop/Midl/include)
</dt> <dt>

[Midl](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[nocode\]**](../midl/nocode.md)
</dt> <dt>

[**\[Ottimizzare\]**](../midl/optimize.md)
</dt> <dt>

[**\[rappresentano \_ come\]**](../midl/represent-as.md)
</dt> <dt>

[**Typedef**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 
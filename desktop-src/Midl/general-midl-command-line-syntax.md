---
title: Sintassi generale della riga di comando MIDL
description: Il compilatore MIDL elabora un file IDL e un file di configurazione dell'applicazione (ACF) facoltativo per generare un set di file di output.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- informazioni di riferimento sulla riga di comando MIDL , sintassi generale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3d3ded263237dffa425cebe3dea49b169e3494045cfc8b0d27cc249c5ebed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384264"
---
# <a name="general-midl-command-line-syntax"></a>Sintassi generale della riga di comando MIDL

Il compilatore MIDL elabora un file IDL e un file di configurazione dell'applicazione (ACF) facoltativo per generare un set di file di output. Gli attributi specificati nell'elenco di attributi di interfaccia del file IDL determinano se il compilatore genera file di origine per un'interfaccia RPC o per un'interfaccia OLE personalizzata.

## <a name="switch-options"></a>Opzioni switch

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*opzione della riga di comando*
</dt> <dd>

Specifica le opzioni della riga di comando del compilatore MIDL. Le opzioni possono essere visualizzate in qualsiasi sequenza.

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*opzioni di opzione*
</dt> <dd>

Specifica le opzioni associate a ogni opzione. Le opzioni valide sono descritte nella voce di riferimento per ogni opzione del compilatore MIDL.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Specifica il nome del file IDL. Questo file ha in genere l'estensione idl, ma può avere un altro file o nessuno.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli elenchi seguenti mostrano i nomi predefiniti dei file generati per un file IDL denominato Name.idl. È possibile usare le opzioni della riga di comando per eseguire l'override di questi nomi predefiniti. Si noti che il nome del file IDL può avere un'estensione diversa da idl o nessuna estensione.

Per impostazione predefinita, ovvero se l'elenco [](object.md) di [](local.md) attributi dell'interfaccia non contiene l'oggetto o l'attributo locale, il compilatore genera i file seguenti per un'interfaccia [RPC:](files-generated-for-an-rpc-interface.md)

-   Stub client (nome \_ c.c)
-   Stub del server \_ (nome s.c)
-   File di intestazione (name.h)

Quando [**l'attributo**](object.md) dell'oggetto viene visualizzato nell'elenco degli attributi dell'interfaccia, il compilatore genera i file seguenti per un'interfaccia COM:

-   File proxy di interfaccia \_ (nome p.c)
-   File di intestazione dell'interfaccia (name.h)
-   File UUID dell'interfaccia \_ (nome I.c)

Quando [**l'attributo locale**](local.md) viene visualizzato nell'elenco degli attributi dell'interfaccia, il compilatore genera solo il file di intestazione dell'interfaccia, Name.h.

Il compilatore MIDL fornito con RPC Microsoft richiama il preprocessore C in base alle esigenze per elaborare il file IDL. Non richiama automaticamente il compilatore C per compilare i file generati.

> [!Note]  
> Il compilatore MIDL fornito con RPC Microsoft usa una sintassi della riga di comando diversa rispetto al compilatore IDL DCE.

 

Le opzioni del compilatore MIDL [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) influiscono sul file stub del server.

A partire da MIDL versione 6.0.359, l'opzione della riga di comando predefinita per il compilatore MIDL è [**/Oicf**](-oi.md)Â [**/robust**](-robust.md). Per disabilitare /robust, specificare [**l'opzione /no \_ robust.**](-no-robust.md)

## <a name="the-header-file"></a>File di intestazione

Il file di intestazione contiene le definizioni di tutti i tipi di dati e di tutte le operazioni dichiarate nel file IDL. Il file di intestazione deve essere incluso da tutti i moduli dell'applicazione che chiamano le operazioni definite, implementano le operazioni definite o modificano i tipi definiti.

Le opzioni /header e [**/out**](-out.md) del [**compilatore**](-header.md) MIDL influiscono sul file di intestazione.

 

 





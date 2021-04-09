---
title: Sintassi della riga di comando MIDL generale
description: Il compilatore MIDL elabora un file IDL e un file di configurazione dell'applicazione (ACF) facoltativo per generare un set di file di output.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- riferimento alla riga di comando MIDL, sintassi generale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856845"
---
# <a name="general-midl-command-line-syntax"></a>Sintassi della riga di comando MIDL generale

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

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*opzioni switch*
</dt> <dd>

Specifica le opzioni associate a ogni opzione. Le opzioni valide sono descritte nella voce di riferimento per ogni opzione del compilatore MIDL.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Specifica il nome del file IDL. Questo file contiene in genere l'estensione IDL, ma può avere un altro o nessuno.

</dd> </dl>

## <a name="remarks"></a>Commenti

Negli elenchi seguenti vengono illustrati i nomi predefiniti dei file generati per un file IDL denominato name. idl. È possibile utilizzare le opzioni della riga di comando per eseguire l'override di questi nomi predefiniti. Si noti che il nome del file IDL può avere un'estensione diversa da IDL oppure nessuna estensione.

Per impostazione predefinita, ovvero se l'elenco di attributi di interfaccia non contiene l' [**oggetto**](object.md) o l'attributo [**locale**](local.md) , il compilatore genera i file seguenti per un' [interfaccia RPC](files-generated-for-an-rpc-interface.md):

-   Stub client (nome \_ c. c)
-   Stub Server (nome \_ s. c)
-   File di intestazione (Name. h)

Quando l'attributo dell' [**oggetto**](object.md) viene visualizzato nell'elenco di attributi di interfaccia, il compilatore genera i file seguenti per un'interfaccia com:

-   File proxy di interfaccia (nome \_ p. c)
-   File di intestazione dell'interfaccia (Name. h)
-   File UUID dell'interfaccia (nome \_ I. c)

Quando l'attributo [**local**](local.md) viene visualizzato nell'elenco di attributi di interfaccia, il compilatore genera solo il file di intestazione dell'interfaccia, Name. h.

Il compilatore MIDL fornito con Microsoft RPC richiama il preprocessore C in base alle esigenze per elaborare il file IDL. Non richiama automaticamente il compilatore C per compilare i file generati.

> [!Note]  
> Il compilatore MIDL fornito con Microsoft RPC usa una sintassi della riga di comando diversa da quella del compilatore IDL DCE.

 

Il compilatore MIDL passa [**/ENV**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) influisce sul file stub del server.

A partire dalla versione MIDL 6.0.359, l'opzione della riga di comando predefinita per il compilatore MIDL è [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md). Per disabilitare/robust, specificare l'opzione [**/No \_ Solid**](-no-robust.md) .

## <a name="the-header-file"></a>Il file di intestazione

Il file di intestazione contiene le definizioni di tutti i tipi di dati e le operazioni dichiarate nel file IDL. Il file di intestazione deve essere incluso in tutti i moduli dell'applicazione che chiamano le operazioni definite, implementano le operazioni definite o modificano i tipi definiti.

Il compilatore MIDL passa [**/header**](-header.md) e [**/out**](-out.md) influisce sul file di intestazione.

 

 





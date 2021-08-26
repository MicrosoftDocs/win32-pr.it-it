---
title: Informazioni di riferimento Command-Line MIDL
description: Questa sezione contiene informazioni di riferimento per ogni opzione della riga di comando e opzione riconosciuta dal compilatore MIDL RPC Microsoft.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Microsoft Interface Definition Language MIDL , riferimento
- MIDL di riferimento alla riga di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df927ded3f1a46045437fe1f9e72e2c7f80dd17d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887350"
---
# <a name="midl-command-line-reference"></a>Informazioni di riferimento Command-Line MIDL

Questa sezione contiene informazioni di riferimento per ogni opzione della riga di comando e opzione riconosciuta dal compilatore MIDL RPC Microsoft. Le voci switch sono disposte in ordine alfabetico. [Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md) che descrive la sintassi della riga di comando generale.

<dl>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)  
[Comando del file di risposta](the-response-file-command.md)  
[**/acf**](-acf.md)  
[**/align**](-align.md)  
[**/amd64**](-amd64.md)  
[**/app \_ config**](-app-config.md)  
[/backward \_ compat](-backward-compat.md)  
[**/c \_ ext**](-c-ext.md)  
[**/caux**](-caux.md)  
[**/char**](-char.md)  
[**/client**](-client.md)  
[**/confirm**](-confirm.md)  
[**/cpp \_ cmd**](-cpp-cmd.md)  
[**/cpp \_ opt**](-cpp-opt.md)  
[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)  
[**/D**](-d.md)  
[**/dlldata**](-dlldata.md)  
[**/env**](-env.md)  
[**/error**](-error.md)  
[**/error**](-error.md)  
[**/h**](-h.md)  
[**/header**](-header.md)  
[**/help (/?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/iid**](-iid.md)  
[**/import**](-import.md)  
[**/lcid**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**/ms \_ ext**](-ms-ext.md)  
[**/ms \_ union**](-ms-union.md)  
[**/msc \_ ver**](-msc-ver.md)  
[**/new**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/no \_ cpp, /nocpp**](-no-cpp-nocpp.md)  
[**/no \_ \_ epv predefinito**](-no-default-epv.md)  
[**/no \_ def \_ idir**](-no-def-idir.md)  
[**/no \_ format \_ opt**](-no-format-opt.md)  
[**/no \_ robust**](-no-robust.md)  
[**/no \_ warn**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/Oi**](-oi.md)  
[**/old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/Os**](-os.md)  
[**/osf**](-osf.md)  
[**/out**](-out.md)  
[**/pack**](-pack.md)  
[**/prefix**](-prefix.md)  
[**/protocol**](-protocol.md)  
[**/proxy**](-proxy.md)  
[**/robust**](-robust.md)  
[**/rpcss**](-rpcss.md)  
[**/sal**](-sal.md)  
[**/sal \_ local**](-sal-local.md)  
[**/saux**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**Controllo \_ /syntax**](-syntax-check.md)  
[**/&lt;Sistema&gt;**](-system-.md)  
[**/target**](-target.md)  
[**/tlb**](-tlb.md)  
[**/U**](-u.md)  
[**/use \_ epv**](-use-epv.md)  
[**/version \_ stamp**](-version-stamp.md)  
[**/W**](-w.md)  
[**/warn**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/Zp**](-zp.md)  
[**/Zs**](-zs.md)  
</dl>

Il compilatore MIDL può generare codice per diverse piattaforme e versioni di sistema. Per altre informazioni sulle opzioni suggerite e su come generare codice ottimizzato per una determinata versione, vedere l'opzione [**/target.**](-target.md)

Si noti che il segno meno (-) può essere sostituito dalla barra (/) in tutte le opzioni della riga di comando MIDL che iniziano con una barra (/). Nell'esempio seguente viene illustrata l'equivalenza quando si richiama il compilatore MIDL.

## <a name="examples"></a>Esempio

**midl /acf my \_ acf.acf** *filename***.idl**

**midl -acf my \_ acf.acf** *filename***.idl**

 

 





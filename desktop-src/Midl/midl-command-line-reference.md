---
title: Informazioni di riferimento Command-Line MIDL
description: Questa sezione contiene informazioni di riferimento per ogni opzione della riga di comando e opzione riconosciuta dal compilatore MIDL RPC Microsoft.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Microsoft Interface Definition Language MIDL , informazioni di riferimento
- informazioni di riferimento sulla riga di comando MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1b7b3182d6a121fb417e5621fe1fb590dba896ebd4d3960b14a99cec3b35af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991204"
---
# <a name="midl-command-line-reference"></a>Informazioni di riferimento Command-Line MIDL

Questa sezione contiene informazioni di riferimento per ogni opzione della riga di comando e opzione riconosciuta dal compilatore MIDL RPC Microsoft. Le voci switch sono disposte in ordine alfabetico. [Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md) descrive la sintassi generale della riga di comando.

<dl>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)  
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
[**/d**](-d.md)  
[**/dlldata**](-dlldata.md)  
[**/env**](-env.md)  
[**/error**](-error.md)  
[**/error**](-error.md)  
[**/h**](-h.md)  
[**/header**](-header.md)  
[**/help (/?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/i**](-i.md)  
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
[**/oi**](-oi.md)  
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
[**/evax**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**/syntax \_ check**](-syntax-check.md)  
[**/<system>**](-system-.md)  
[**/target**](-target.md)  
[**/tlb**](-tlb.md)  
[**/u**](-u.md)  
[**/use \_ epv**](-use-epv.md)  
[**/version \_ stamp**](-version-stamp.md)  
[**/w**](-w.md)  
[**/warn**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/wx**](-wx.md)  
[**/Zp**](-zp.md)  
[**/Zs**](-zs.md)  
</dl>

Il compilatore MIDL può generare codice per piattaforme e versioni di sistema diverse. Consultare [**l'opzione /target**](-target.md) per altre informazioni sulle opzioni suggerite e su come generare codice ottimizzato per una determinata versione.

Si noti che il segno meno (-) può essere sostituito dalla barra (/) in tutte le opzioni della riga di comando MIDL che iniziano con una barra (/). Nell'esempio seguente viene illustrata l'equivalenza quando si richiama il compilatore MIDL.

## <a name="examples"></a>Esempio

**midl /acf my \_ acf.acf** *filename***.idl**

**midl -acf my \_ acf.acf** *filename***.idl**

 

 





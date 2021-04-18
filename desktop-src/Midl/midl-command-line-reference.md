---
title: Riferimento Command-Line MIDL
description: Questa sezione contiene informazioni di riferimento per ogni opzione della riga di comando e opzione di commutazione riconosciuta dal compilatore MIDL di Microsoft RPC.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Microsoft Interface Definition Language MIDL, riferimento
- riferimento alla riga di comando MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106302806"
---
# <a name="midl-command-line-reference"></a>Riferimento Command-Line MIDL

Questa sezione contiene informazioni di riferimento per ogni opzione della riga di comando e opzione di commutazione riconosciuta dal compilatore MIDL di Microsoft RPC. Le voci di cambio sono disposte in ordine alfabetico. La [sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md) descrive la sintassi della riga di comando generale.

<dl>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)  
[Comando del file di risposta](the-response-file-command.md)  
[**/acf**](-acf.md)  
[**/align**](-align.md)  
[**/amd64**](-amd64.md)  
[**configurazione di/app \_**](-app-config.md)  
[\_compatibilità/backward](-backward-compat.md)  
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
[**/ENV**](-env.md)  
[**/Error**](-error.md)  
[**/Error**](-error.md)  
[**/h**](-h.md)  
[**/header**](-header.md)  
[**/Help (/?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/IID**](-iid.md)  
[**/Import**](-import.md)  
[**/LCID**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**/MS \_ ext**](-ms-ext.md)  
[**\_Unione/MS**](-ms-union.md)  
[**/MSC \_ ver**](-msc-ver.md)  
[**/New**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/No \_ cpp,/nocpp**](-no-cpp-nocpp.md)  
[**/No \_ default \_ EPV**](-no-default-epv.md)  
[**/No \_ def \_ Idir**](-no-def-idir.md)  
[**/No \_ Format \_ opz**](-no-format-opt.md)  
[**/No \_ affidabile**](-no-robust.md)  
[**avviso di/no \_**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/OI**](-oi.md)  
[**/Old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/OS**](-os.md)  
[**/osf**](-osf.md)  
[**/out**](-out.md)  
[**/Pack**](-pack.md)  
[**/prefix**](-prefix.md)  
[**/protocol**](-protocol.md)  
[**/proxy**](-proxy.md)  
[**/Robust**](-robust.md)  
[**/rpcss**](-rpcss.md)  
[**/sal**](-sal.md)  
[**/SAL \_ locale**](-sal-local.md)  
[**/saux**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**\_controllo/Syntax**](-syntax-check.md)  
[**/<system>**](-system-.md)  
[**/target**](-target.md)  
[**/TLB**](-tlb.md)  
[**/U**](-u.md)  
[**\_EPV/utilizza**](-use-epv.md)  
[**\_timbro/Version**](-version-stamp.md)  
[**/W**](-w.md)  
[**/warn**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/ZP**](-zp.md)  
[**/ZS**](-zs.md)  
</dl>

Il compilatore MIDL può generare codice per diverse piattaforme e versioni di sistema. Per ulteriori informazioni sulle opzioni suggerite e su come generare codice ottimizzato per una determinata versione, vedere l'opzione [**/target**](-target.md) .

Si noti che il segno meno (–) può essere sostituito con la barra (/) in tutte le opzioni della riga di comando MIDL che iniziano con una barra (/). Nell'esempio seguente viene illustrata l'equivalenza quando si richiama il compilatore MIDL.

## <a name="examples"></a>Esempio

**MIDL/ACF My \_ ACF. ACF** *nomefile * * *. idl**

**MIDL-ACF nome file ACF \_ . ACF** ** * *. idl**

 

 





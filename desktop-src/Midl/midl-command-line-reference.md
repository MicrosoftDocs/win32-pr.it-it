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
# <a name="midl-command-line-reference"></a><span data-ttu-id="45e69-105">Riferimento Command-Line MIDL</span><span class="sxs-lookup"><span data-stu-id="45e69-105">MIDL Command-Line Reference</span></span>

<span data-ttu-id="45e69-106">Questa sezione contiene informazioni di riferimento per ogni opzione della riga di comando e opzione di commutazione riconosciuta dal compilatore MIDL di Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="45e69-106">This section contains reference information for each command-line switch and switch option recognized by the Microsoft RPC MIDL compiler.</span></span> <span data-ttu-id="45e69-107">Le voci di cambio sono disposte in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="45e69-107">Switch entries are arranged in alphabetical order.</span></span> <span data-ttu-id="45e69-108">La [sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md) descrive la sintassi della riga di comando generale.</span><span class="sxs-lookup"><span data-stu-id="45e69-108">[General MIDL Command-line Syntax](general-midl-command-line-syntax.md) describes the general command-line syntax.</span></span>

<dl>

[<span data-ttu-id="45e69-109">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="45e69-109">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)  
[<span data-ttu-id="45e69-110">Comando del file di risposta</span><span class="sxs-lookup"><span data-stu-id="45e69-110">The Response File Command</span></span>](the-response-file-command.md)  
[<span data-ttu-id="45e69-111">**/acf**</span><span class="sxs-lookup"><span data-stu-id="45e69-111">**/acf**</span></span>](-acf.md)  
[<span data-ttu-id="45e69-112">**/align**</span><span class="sxs-lookup"><span data-stu-id="45e69-112">**/align**</span></span>](-align.md)  
[<span data-ttu-id="45e69-113">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="45e69-113">**/amd64**</span></span>](-amd64.md)  
[<span data-ttu-id="45e69-114">**configurazione di/app \_**</span><span class="sxs-lookup"><span data-stu-id="45e69-114">**/app\_config**</span></span>](-app-config.md)  
[<span data-ttu-id="45e69-115">\_compatibilità/backward</span><span class="sxs-lookup"><span data-stu-id="45e69-115">/backward\_compat</span></span>](-backward-compat.md)  
[<span data-ttu-id="45e69-116">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="45e69-116">**/c\_ext**</span></span>](-c-ext.md)  
[<span data-ttu-id="45e69-117">**/caux**</span><span class="sxs-lookup"><span data-stu-id="45e69-117">**/caux**</span></span>](-caux.md)  
[<span data-ttu-id="45e69-118">**/char**</span><span class="sxs-lookup"><span data-stu-id="45e69-118">**/char**</span></span>](-char.md)  
[<span data-ttu-id="45e69-119">**/client**</span><span class="sxs-lookup"><span data-stu-id="45e69-119">**/client**</span></span>](-client.md)  
[<span data-ttu-id="45e69-120">**/confirm**</span><span class="sxs-lookup"><span data-stu-id="45e69-120">**/confirm**</span></span>](-confirm.md)  
[<span data-ttu-id="45e69-121">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="45e69-121">**/cpp\_cmd**</span></span>](-cpp-cmd.md)  
[<span data-ttu-id="45e69-122">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="45e69-122">**/cpp\_opt**</span></span>](-cpp-opt.md)  
<span data-ttu-id="45e69-123">[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)</span><span class="sxs-lookup"><span data-stu-id="45e69-123">[**/cstruct_out**](-cstruct-out.md)
[**/cstub**](-cstub.md)</span></span>  
[<span data-ttu-id="45e69-124">**/D**</span><span class="sxs-lookup"><span data-stu-id="45e69-124">**/D**</span></span>](-d.md)  
[<span data-ttu-id="45e69-125">**/dlldata**</span><span class="sxs-lookup"><span data-stu-id="45e69-125">**/dlldata**</span></span>](-dlldata.md)  
[<span data-ttu-id="45e69-126">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="45e69-126">**/env**</span></span>](-env.md)  
[<span data-ttu-id="45e69-127">**/Error**</span><span class="sxs-lookup"><span data-stu-id="45e69-127">**/error**</span></span>](-error.md)  
[<span data-ttu-id="45e69-128">**/Error**</span><span class="sxs-lookup"><span data-stu-id="45e69-128">**/error**</span></span>](-error.md)  
[<span data-ttu-id="45e69-129">**/h**</span><span class="sxs-lookup"><span data-stu-id="45e69-129">**/h**</span></span>](-h.md)  
[<span data-ttu-id="45e69-130">**/header**</span><span class="sxs-lookup"><span data-stu-id="45e69-130">**/header**</span></span>](-header.md)  
[<span data-ttu-id="45e69-131">**/Help (/?)**</span><span class="sxs-lookup"><span data-stu-id="45e69-131">**/help (/?)**</span></span>](-help-.md)  
[<span data-ttu-id="45e69-132">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="45e69-132">**/ia64**</span></span>](-ia64.md)  
[<span data-ttu-id="45e69-133">**/I**</span><span class="sxs-lookup"><span data-stu-id="45e69-133">**/I**</span></span>](-i.md)  
[<span data-ttu-id="45e69-134">**/IID**</span><span class="sxs-lookup"><span data-stu-id="45e69-134">**/iid**</span></span>](-iid.md)  
[<span data-ttu-id="45e69-135">**/Import**</span><span class="sxs-lookup"><span data-stu-id="45e69-135">**/import**</span></span>](-import.md)  
[<span data-ttu-id="45e69-136">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="45e69-136">**/lcid**</span></span>](-lcid.md)  
[<span data-ttu-id="45e69-137">**/mktyplib203**</span><span class="sxs-lookup"><span data-stu-id="45e69-137">**/mktyplib203**</span></span>](-mktyplib203.md)  
[<span data-ttu-id="45e69-138">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="45e69-138">**/ms\_ext**</span></span>](-ms-ext.md)  
[<span data-ttu-id="45e69-139">**\_Unione/MS**</span><span class="sxs-lookup"><span data-stu-id="45e69-139">**/ms\_union**</span></span>](-ms-union.md)  
[<span data-ttu-id="45e69-140">**/MSC \_ ver**</span><span class="sxs-lookup"><span data-stu-id="45e69-140">**/msc\_ver**</span></span>](-msc-ver.md)  
[<span data-ttu-id="45e69-141">**/New**</span><span class="sxs-lookup"><span data-stu-id="45e69-141">**/new**</span></span>](-new.md)  
[<span data-ttu-id="45e69-142">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="45e69-142">**/newtlb**</span></span>](-newtlb.md)  
[<span data-ttu-id="45e69-143">**/No \_ cpp,/nocpp**</span><span class="sxs-lookup"><span data-stu-id="45e69-143">**/no\_cpp, /nocpp**</span></span>](-no-cpp-nocpp.md)  
[<span data-ttu-id="45e69-144">**/No \_ default \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="45e69-144">**/no\_default\_epv**</span></span>](-no-default-epv.md)  
[<span data-ttu-id="45e69-145">**/No \_ def \_ Idir**</span><span class="sxs-lookup"><span data-stu-id="45e69-145">**/no\_def\_idir**</span></span>](-no-def-idir.md)  
[<span data-ttu-id="45e69-146">**/No \_ Format \_ opz**</span><span class="sxs-lookup"><span data-stu-id="45e69-146">**/no\_format\_opt**</span></span>](-no-format-opt.md)  
[<span data-ttu-id="45e69-147">**/No \_ affidabile**</span><span class="sxs-lookup"><span data-stu-id="45e69-147">**/no\_robust**</span></span>](-no-robust.md)  
[<span data-ttu-id="45e69-148">**avviso di/no \_**</span><span class="sxs-lookup"><span data-stu-id="45e69-148">**/no\_warn**</span></span>](-no-warn.md)  
[<span data-ttu-id="45e69-149">**/nologo**</span><span class="sxs-lookup"><span data-stu-id="45e69-149">**/nologo**</span></span>](-nologo.md)  
[<span data-ttu-id="45e69-150">**/notlb**</span><span class="sxs-lookup"><span data-stu-id="45e69-150">**/notlb**</span></span>](-notlb.md)  
[<span data-ttu-id="45e69-151">**/o**</span><span class="sxs-lookup"><span data-stu-id="45e69-151">**/o**</span></span>](-o.md)  
[<span data-ttu-id="45e69-152">**/OI**</span><span class="sxs-lookup"><span data-stu-id="45e69-152">**/Oi**</span></span>](-oi.md)  
[<span data-ttu-id="45e69-153">**/Old**</span><span class="sxs-lookup"><span data-stu-id="45e69-153">**/old**</span></span>](-old.md)  
[<span data-ttu-id="45e69-154">**/oldtlb**</span><span class="sxs-lookup"><span data-stu-id="45e69-154">**/oldtlb**</span></span>](-oldtlb.md)  
[<span data-ttu-id="45e69-155">**/oldnames**</span><span class="sxs-lookup"><span data-stu-id="45e69-155">**/oldnames**</span></span>](-oldnames.md)  
[<span data-ttu-id="45e69-156">**/OS**</span><span class="sxs-lookup"><span data-stu-id="45e69-156">**/Os**</span></span>](-os.md)  
[<span data-ttu-id="45e69-157">**/osf**</span><span class="sxs-lookup"><span data-stu-id="45e69-157">**/osf**</span></span>](-osf.md)  
[<span data-ttu-id="45e69-158">**/out**</span><span class="sxs-lookup"><span data-stu-id="45e69-158">**/out**</span></span>](-out.md)  
[<span data-ttu-id="45e69-159">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="45e69-159">**/pack**</span></span>](-pack.md)  
[<span data-ttu-id="45e69-160">**/prefix**</span><span class="sxs-lookup"><span data-stu-id="45e69-160">**/prefix**</span></span>](-prefix.md)  
[<span data-ttu-id="45e69-161">**/protocol**</span><span class="sxs-lookup"><span data-stu-id="45e69-161">**/protocol**</span></span>](-protocol.md)  
[<span data-ttu-id="45e69-162">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="45e69-162">**/proxy**</span></span>](-proxy.md)  
[<span data-ttu-id="45e69-163">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="45e69-163">**/robust**</span></span>](-robust.md)  
[<span data-ttu-id="45e69-164">**/rpcss**</span><span class="sxs-lookup"><span data-stu-id="45e69-164">**/rpcss**</span></span>](-rpcss.md)  
[<span data-ttu-id="45e69-165">**/sal**</span><span class="sxs-lookup"><span data-stu-id="45e69-165">**/sal**</span></span>](-sal.md)  
[<span data-ttu-id="45e69-166">**/SAL \_ locale**</span><span class="sxs-lookup"><span data-stu-id="45e69-166">**/sal\_local**</span></span>](-sal-local.md)  
[<span data-ttu-id="45e69-167">**/saux**</span><span class="sxs-lookup"><span data-stu-id="45e69-167">**/saux**</span></span>](-saux.md)  
[<span data-ttu-id="45e69-168">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="45e69-168">**/savePP**</span></span>](-savepp.md)  
[<span data-ttu-id="45e69-169">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="45e69-169">**/sstub**</span></span>](-sstub.md)  
[<span data-ttu-id="45e69-170">**\_controllo/Syntax**</span><span class="sxs-lookup"><span data-stu-id="45e69-170">**/syntax\_check**</span></span>](-syntax-check.md)  
[**/<system>**](-system-.md)  
[<span data-ttu-id="45e69-171">**/target**</span><span class="sxs-lookup"><span data-stu-id="45e69-171">**/target**</span></span>](-target.md)  
[<span data-ttu-id="45e69-172">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="45e69-172">**/tlb**</span></span>](-tlb.md)  
[<span data-ttu-id="45e69-173">**/U**</span><span class="sxs-lookup"><span data-stu-id="45e69-173">**/U**</span></span>](-u.md)  
[<span data-ttu-id="45e69-174">**\_EPV/utilizza**</span><span class="sxs-lookup"><span data-stu-id="45e69-174">**/use\_epv**</span></span>](-use-epv.md)  
[<span data-ttu-id="45e69-175">**\_timbro/Version**</span><span class="sxs-lookup"><span data-stu-id="45e69-175">**/version\_stamp**</span></span>](-version-stamp.md)  
[<span data-ttu-id="45e69-176">**/W**</span><span class="sxs-lookup"><span data-stu-id="45e69-176">**/W**</span></span>](-w.md)  
[<span data-ttu-id="45e69-177">**/warn**</span><span class="sxs-lookup"><span data-stu-id="45e69-177">**/warn**</span></span>](-warn.md)  
[<span data-ttu-id="45e69-178">**/win32**</span><span class="sxs-lookup"><span data-stu-id="45e69-178">**/win32**</span></span>](-win32.md)  
[<span data-ttu-id="45e69-179">**/win64**</span><span class="sxs-lookup"><span data-stu-id="45e69-179">**/win64**</span></span>](-win64.md)  
[<span data-ttu-id="45e69-180">**/WX**</span><span class="sxs-lookup"><span data-stu-id="45e69-180">**/WX**</span></span>](-wx.md)  
[<span data-ttu-id="45e69-181">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="45e69-181">**/Zp**</span></span>](-zp.md)  
[<span data-ttu-id="45e69-182">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="45e69-182">**/Zs**</span></span>](-zs.md)  
</dl>

<span data-ttu-id="45e69-183">Il compilatore MIDL può generare codice per diverse piattaforme e versioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="45e69-183">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="45e69-184">Per ulteriori informazioni sulle opzioni suggerite e su come generare codice ottimizzato per una determinata versione, vedere l'opzione [**/target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="45e69-184">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a given release.</span></span>

<span data-ttu-id="45e69-185">Si noti che il segno meno (–) può essere sostituito con la barra (/) in tutte le opzioni della riga di comando MIDL che iniziano con una barra (/).</span><span class="sxs-lookup"><span data-stu-id="45e69-185">Note that the minus sign (–) may be substituted for the slash (/) in all MIDL command-line switches that begin with a slash (/).</span></span> <span data-ttu-id="45e69-186">Nell'esempio seguente viene illustrata l'equivalenza quando si richiama il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="45e69-186">The following example demonstrates their equivalence when invoking the MIDL compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="45e69-187">Esempio</span><span class="sxs-lookup"><span data-stu-id="45e69-187">Examples</span></span>

<span data-ttu-id="45e69-188">**MIDL/ACF My \_ ACF. ACF** *nomefile \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="45e69-188">**midl /acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

<span data-ttu-id="45e69-189">**MIDL-ACF nome file ACF \_ . ACF** \*\* \* *. idl*\*</span><span class="sxs-lookup"><span data-stu-id="45e69-189">**midl -acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

 

 





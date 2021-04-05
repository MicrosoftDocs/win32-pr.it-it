---
description: Pktextract.exe è uno strumento che estrae l'attributo publicKeyToken da un file di certificato.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131302"
---
# <a name="pktextractexe"></a><span data-ttu-id="a71f2-103">Pktextract.exe</span><span class="sxs-lookup"><span data-stu-id="a71f2-103">Pktextract.exe</span></span>

<span data-ttu-id="a71f2-104">Pktextract.exe è uno strumento che estrae l'attributo **PublicKeyToken** da un file di certificato.</span><span class="sxs-lookup"><span data-stu-id="a71f2-104">Pktextract.exe is a tool that extracts the **publicKeyToken** attribute from a certificate file.</span></span> <span data-ttu-id="a71f2-105">L'output è **PublicKeyToken**, ovvero un identificatore univoco a 16 caratteri (8 byte) della chiave pubblica presente nel certificato, in un formato che può essere facilmente incollato in un'istruzione di identità dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="a71f2-105">The output is the **publicKeyToken**, which is a unique 16-character (8-byte) identifier of the public key present in the certificate, in a format that can easily be pasted into an assembly identity statement.</span></span> <span data-ttu-id="a71f2-106">Il file del certificato deve essere presente nella stessa directory del Pktextract.exe per utilizzare l'utilità.</span><span class="sxs-lookup"><span data-stu-id="a71f2-106">The certificate file must be present in the same directory as Pktextract.exe to use the utility.</span></span> <span data-ttu-id="a71f2-107">Pktextract.exe è disponibile nel Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a71f2-107">Pktextract.exe is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="a71f2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a71f2-108">Syntax</span></span>

<span data-ttu-id="a71f2-109">**pktextract.exe** *<nomefile. cer>* **\[ -quiet \] \[ -nologo \]**</span><span class="sxs-lookup"><span data-stu-id="a71f2-109">**pktextract.exe** *<filename.cer>* **\[-quiet\] \[-nologo\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="a71f2-110">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="a71f2-110">Command Line Options</span></span>

<span data-ttu-id="a71f2-111">Pktextract.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a71f2-111">Pktextract.exe uses the following case-insensitive command line options.</span></span>



| <span data-ttu-id="a71f2-112">Opzione</span><span class="sxs-lookup"><span data-stu-id="a71f2-112">Option</span></span>  | <span data-ttu-id="a71f2-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a71f2-113">Description</span></span>                                                          |
|---------|----------------------------------------------------------------------|
| <span data-ttu-id="a71f2-114">-quiet</span><span class="sxs-lookup"><span data-stu-id="a71f2-114">-quiet</span></span>  | <span data-ttu-id="a71f2-115">Evita la visualizzazione completa delle informazioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="a71f2-115">Suppresses full display of certificate information.</span></span> <span data-ttu-id="a71f2-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a71f2-116">Optional.</span></span>        |
| <span data-ttu-id="a71f2-117">-nologo</span><span class="sxs-lookup"><span data-stu-id="a71f2-117">-nologo</span></span> | <span data-ttu-id="a71f2-118">Viene eseguito senza visualizzare i dati di copyright Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="a71f2-118">Runs without displaying standard Microsoft copyright data.</span></span> <span data-ttu-id="a71f2-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a71f2-119">Optional.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a71f2-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a71f2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a71f2-121">Strumenti di sviluppo di assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="a71f2-121">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




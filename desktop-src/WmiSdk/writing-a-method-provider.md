---
description: Un provider di metodi consente l'accesso WMI ai metodi di una classe. Ad esempio, una classe che rappresenta un'applicazione può disporre di un metodo che termina l'applicazione.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Scrittura di un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310317"
---
# <a name="writing-a-method-provider"></a><span data-ttu-id="22a33-104">Scrittura di un provider di metodi</span><span class="sxs-lookup"><span data-stu-id="22a33-104">Writing a Method Provider</span></span>

<span data-ttu-id="22a33-105">Un provider di metodi consente l'accesso WMI ai metodi di una classe.</span><span class="sxs-lookup"><span data-stu-id="22a33-105">A method provider allows WMI access to the methods of a class.</span></span> <span data-ttu-id="22a33-106">Ad esempio, una classe che rappresenta un'applicazione può disporre di un metodo che termina l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="22a33-106">For example, a class that represents an application may have a method that terminates the application.</span></span>

<span data-ttu-id="22a33-107">La modifica dell'ordine dei parametri di input e output del metodo durante l'aggiornamento di un provider di metodi esistente può causare un errore per le applicazioni che chiamano il metodo.</span><span class="sxs-lookup"><span data-stu-id="22a33-107">Changing the order of method input and output parameters when updating an existing method provider can cause failure for applications that call the method.</span></span> <span data-ttu-id="22a33-108">L'ordine dei parametri di input o output viene stabilito dal valore del qualificatore [**ID**](standard-wmi-qualifiers.md) per ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="22a33-108">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="22a33-109">Il primo parametro ha un valore **ID** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="22a33-109">The first parameter has an **ID** value of zero.</span></span> <span data-ttu-id="22a33-110">Aggiungere nuovi parametri di input alla fine dei parametri esistenti anziché inserirli nella sequenza già stabilita.</span><span class="sxs-lookup"><span data-stu-id="22a33-110">Add new input parameters at the end of the existing parameters rather than inserting them in the already established sequence.</span></span>

<span data-ttu-id="22a33-111">Nella procedura seguente viene descritto come implementare un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="22a33-111">The following procedure describes how to implement a method provider.</span></span>

<span data-ttu-id="22a33-112">**Per implementare un provider di metodi**</span><span class="sxs-lookup"><span data-stu-id="22a33-112">**To implement a method provider**</span></span>

1.  <span data-ttu-id="22a33-113">Progettare e registrare il provider di classi con WMI.</span><span class="sxs-lookup"><span data-stu-id="22a33-113">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="22a33-114">I provider di classi si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="22a33-114">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class.</span></span> <span data-ttu-id="22a33-115">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di metodi](registering-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22a33-115">For more information, see [Registering a Method Provider](registering-a-method-provider.md).</span></span>

2.  <span data-ttu-id="22a33-116">Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.</span><span class="sxs-lookup"><span data-stu-id="22a33-116">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    > [!Note]  
    > <span data-ttu-id="22a33-117">I provider di metodi sono vivamente invitati a usare il modello di multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="22a33-117">Method providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="22a33-118">Implementare il metodo [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) per il provider.</span><span class="sxs-lookup"><span data-stu-id="22a33-118">Implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method for your provider.</span></span>

    <span data-ttu-id="22a33-119">L'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è l'interfaccia principale per un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="22a33-119">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a method provider.</span></span> <span data-ttu-id="22a33-120">Per ulteriori informazioni, vedere [implementazione dell'interfaccia primaria per un provider di metodi](implementing-the-primary-interface-for-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22a33-120">For more information, see [Implementing the Primary Interface for a Method Provider](implementing-the-primary-interface-for-a-method-provider.md).</span></span>

4.  <span data-ttu-id="22a33-121">Aggiungere il codice aggiuntivo necessario per il provider.</span><span class="sxs-lookup"><span data-stu-id="22a33-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="22a33-122">Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI.</span><span class="sxs-lookup"><span data-stu-id="22a33-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="22a33-123">Per ulteriori informazioni, vedere [chiamata di un metodo](calling-a-method.md) e [gestione dei livelli di sicurezza in un provider](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="22a33-123">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="22a33-124">Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client.</span><span class="sxs-lookup"><span data-stu-id="22a33-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="22a33-125">Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="22a33-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="22a33-126">Sostituire il provider preesistente con il nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="22a33-126">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="22a33-127">Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia.</span><span class="sxs-lookup"><span data-stu-id="22a33-127">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="22a33-128">Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22a33-128">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 




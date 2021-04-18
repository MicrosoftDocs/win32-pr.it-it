---
description: Consente di registrare un computer in una gerarchia di certificati utilizzando un modello, un nome visualizzato del certificato e la descrizione del certificato.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313719"
---
# <a name="enrollsimplemachinecert"></a><span data-ttu-id="05743-103">enrollSimpleMachineCert</span><span class="sxs-lookup"><span data-stu-id="05743-103">enrollSimpleMachineCert</span></span>

<span data-ttu-id="05743-104">Nell'esempio enrollSimpleMachineCert viene registrato un computer in una gerarchia di certificati utilizzando un modello, un nome visualizzato del certificato e la descrizione del certificato.</span><span class="sxs-lookup"><span data-stu-id="05743-104">The enrollSimpleMachineCert sample enrolls a computer in a certificate hierarchy by using a template, a certificate display name, and the certificate description.</span></span>

## <a name="location"></a><span data-ttu-id="05743-105">Location</span><span class="sxs-lookup"><span data-stu-id="05743-105">Location</span></span>

<span data-ttu-id="05743-106">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, per impostazione predefinita viene installata una versione C++ dell'esempio, nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate di registrazione del certificato \\ VC \\ EnrollSimpleMachineCert.</span><span class="sxs-lookup"><span data-stu-id="05743-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\EnrollSimpleMachineCert folder.</span></span> <span data-ttu-id="05743-107">Una versione di VBScript viene installata nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registrazione del certificato \\ vbs \\ EnrollSimpleMachineCert.</span><span class="sxs-lookup"><span data-stu-id="05743-107">A VBScript version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VBS\\EnrollSimpleMachineCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="05743-108">Discussione</span><span class="sxs-lookup"><span data-stu-id="05743-108">Discussion</span></span>

<span data-ttu-id="05743-109">Esempio enrollSimpleMachineCert:</span><span class="sxs-lookup"><span data-stu-id="05743-109">The enrollSimpleMachineCert sample:</span></span>

1.  <span data-ttu-id="05743-110">Elabora gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="05743-110">Processes the command line arguments.</span></span> <span data-ttu-id="05743-111">La riga di comando deve contenere il nome del modello, un nome visualizzato del certificato e una descrizione del certificato.</span><span class="sxs-lookup"><span data-stu-id="05743-111">The command line should contain the name of the template, a certificate display name, and a certificate description.</span></span>
2.  <span data-ttu-id="05743-112">Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e lo inizializza usando il modello specificato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="05743-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template specified on the command line.</span></span> <span data-ttu-id="05743-113">Il valore ContextAdministratorForceMachine per il primo parametro specifica che il certificato viene richiesto da un amministratore che agisce per conto di un computer.</span><span class="sxs-lookup"><span data-stu-id="05743-113">The ContextAdministratorForceMachine value for the first parameter specifies that the certificate is being requested by an administrator acting on behalf of a computer.</span></span>
3.  <span data-ttu-id="05743-114">Aggiunge il nome visualizzato e la descrizione all'oggetto di registrazione.</span><span class="sxs-lookup"><span data-stu-id="05743-114">Adds the display name and description to the enrollment object.</span></span>
4.  <span data-ttu-id="05743-115">Tenta di registrare la richiesta di certificato e controlla lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="05743-115">Attempts to enroll the certificate request and checks the status of the process.</span></span> <span data-ttu-id="05743-116">La funzione checkEnrollStatus è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="05743-116">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05743-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05743-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05743-118">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="05743-118">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 




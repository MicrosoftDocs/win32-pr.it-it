---
description: Individuazione di risorse PE non Win32
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Individuazione di risorse PE non Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308703"
---
# <a name="locating-non-win32-pe-resources"></a><span data-ttu-id="668fc-103">Individuazione di risorse PE non Win32</span><span class="sxs-lookup"><span data-stu-id="668fc-103">Locating Non-Win32 PE Resources</span></span>

<span data-ttu-id="668fc-104">Per individuare le risorse PE non Win32, l'applicazione deve prima chiamare la funzione [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) per individuare il file di risorse specifico della lingua da cui caricare le risorse.</span><span class="sxs-lookup"><span data-stu-id="668fc-104">To locate non-Win32 PE resources, your application should first call the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function to locate the language-specific resource file from which to load resources.</span></span> <span data-ttu-id="668fc-105">Se l'applicazione segue le impostazioni della lingua di sistema, deve chiamare la funzione con il \_ nome del linguaggio MUI \_ \| MUI \_ utente \_ preferenza lingue dell'interfaccia utente \_ \_ specificata per *dwFlags* e **null** specificato per *pwszLanguage*.</span><span class="sxs-lookup"><span data-stu-id="668fc-105">If the application is following system language settings, it must call the function with MUI\_LANGUAGE\_NAME \| MUI\_USER\_PREFERRED\_UI\_LANGUAGES specified for *dwFlags* and **NULL** specified for *pwszLanguage*.</span></span> <span data-ttu-id="668fc-106">Se l'applicazione segue le impostazioni della lingua specifica dell'applicazione, USA **GetFileMUIPath** per determinare se esiste un file specifico della lingua specificando la lingua nel parametro *pwszLanguage* .</span><span class="sxs-lookup"><span data-stu-id="668fc-106">If the application is following application-specific language settings, it uses **GetFileMUIPath** to determine if a language-specific file exists by specifying the language in the *pwszLanguage* parameter.</span></span>

<span data-ttu-id="668fc-107">Dopo la chiamata a [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), l'applicazione deve definire funzionalità personalizzate per caricare il modulo della risorsa e caricare risorse specifiche.</span><span class="sxs-lookup"><span data-stu-id="668fc-107">After the call to [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), the application must define custom functionality to load the resource module and load specific resources from it.</span></span> <span data-ttu-id="668fc-108">Se, ad esempio, si utilizza un file di risorse con estensione txt o XML, l'applicazione deve utilizzare un parser TXT o XML per caricare il file e quindi analizzare il contenuto del file per ogni risorsa richiesta.</span><span class="sxs-lookup"><span data-stu-id="668fc-108">For example, if you are using a .txt or .xml resource file, the application must use a TXT or XML parser to load the file and then parse the contents of the file for each required resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="668fc-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="668fc-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="668fc-110">Uso dell'interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="668fc-110">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="668fc-111">**GetFileMUIPath**</span><span class="sxs-lookup"><span data-stu-id="668fc-111">**GetFileMUIPath**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 




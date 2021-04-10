---
title: Accesso ai servizi tramite Java
description: Accesso ai servizi tramite Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c24ae7508b5999e5d07f2480d49cb4c20dd89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956403"
---
# <a name="accessing-services-using-java"></a><span data-ttu-id="45803-103">Accesso ai servizi tramite Java</span><span class="sxs-lookup"><span data-stu-id="45803-103">Accessing Services Using Java</span></span>

<span data-ttu-id="45803-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="45803-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="45803-105">È anche possibile accedere ai servizi di Microsoft Agent da un'applet Java.</span><span class="sxs-lookup"><span data-stu-id="45803-105">You can also access Microsoft Agent services from a Java applet.</span></span> <span data-ttu-id="45803-106">Molte delle funzioni accessibili tramite le interfacce di Microsoft Agent restituiscono valori tramite parametri passati per riferimento.</span><span class="sxs-lookup"><span data-stu-id="45803-106">Many of the functions accessible through the Microsoft Agent interfaces return values through parameters passed by reference.</span></span> <span data-ttu-id="45803-107">Per passare questi parametri da Java, è necessario creare matrici a elemento singolo nel codice e passarle come parametri alla funzione appropriata.</span><span class="sxs-lookup"><span data-stu-id="45803-107">In order to pass these parameters from Java, it is necessary to create single-element arrays in your code and pass them as parameters to the appropriate function.</span></span> <span data-ttu-id="45803-108">Se si utilizza Microsoft Visual J++ ed è stata eseguita la procedura guidata libreria dei tipi Java nel server Microsoft Agent, fare riferimento al file summary.txt per verificare quali funzioni richiedono argomenti di matrice.</span><span class="sxs-lookup"><span data-stu-id="45803-108">If you are using Microsoft Visual J++ and have run the Java Type Library Wizard on the Microsoft Agent server, refer to the summary.txt file to review which functions require array arguments.</span></span> <span data-ttu-id="45803-109">La procedura è simile a quella in C; usare l'interfaccia [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) per creare un'istanza del server e quindi caricare il carattere:</span><span class="sxs-lookup"><span data-stu-id="45803-109">The procedure is similar to that in C; you use the [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) interface to create an instance of the server, then load the character:</span></span>


```
private IAgentEx            m_AgentEx = null;
private IAgentCharacterEx   m_Merlin[] = {null};
private int                 m_MerlinID[] = {-1};
private int                 m_RequestID[] = {0};
private final String        m_CharacterPath = "merlin.acs";

public void start()
{
      // Start the Microsoft Agent Server

      m_AgentEx = (IAgentEx) new AgentServer();

      try
      {

         Variant characterPath = new Variant();
         characterPath.putString(m_CharacterPath);

         // Load the character

         m_AgentEx.Load(characterPath,
                    m_MerlinID,
                    m_RequestID);
      }
```



<span data-ttu-id="45803-110">La procedura è leggermente diversa durante il caricamento di caratteri da una posizione remota HTTP, ad esempio un sito Web.</span><span class="sxs-lookup"><span data-stu-id="45803-110">The procedure is slightly different when loading characters from a HTTP remote location such as a website.</span></span> <span data-ttu-id="45803-111">In questo caso il metodo [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) è asincrono e genererà un'eccezione com di e \_ in sospeso (0x8000000A).</span><span class="sxs-lookup"><span data-stu-id="45803-111">In this case the [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) method is asynchronous and will raise a COM exception of E\_PENDING (0x8000000a).</span></span> <span data-ttu-id="45803-112">Sarà necessario intercettare questa eccezione e gestirla correttamente, come avviene nelle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="45803-112">You will need to catch this exception and handle it correctly as is done in the following functions:</span></span>


```
// Constants used in asynchronous character loads

private final int E_PENDING = 0x8000000a;
private final int NOERROR = 0;


// This function loads a character from the specified path.
// It correctly handles the loading of characters from
// remote sites.

// This sample doesn't care about the request id returned
// from the Load call.  Real production code might use the
// request id and the RequestComplete callback to check for
// a successful character load before proceeding.

public int LoadCharacter(Variant path, int[] id)
{
   int requestid[] = {-1};
   int hRes = 0;

   try
   {
      // Load the character

      m_AgentEx.Load(path, id, requestid);
   }
   catch(com.ms.com.ComException e)
   {
      // Get the HRESULT

      hRes = e.getHResult();
      
      // If the error code is E_PENDING, we return NOERROR

      if (hRes == E_PENDING)
         hRes = NOERROR;
   }

   return hRes;
}

public void start()
{
   if (LoadCharacter(characterPath, m_MerlinID) != NOERROR)
   {
      stop();
      return;
   }

   // Other initialization code here

   .
   .
   .
}
```



<span data-ttu-id="45803-113">Ottenere quindi l'interfaccia [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) che consente di accedere ai relativi metodi:</span><span class="sxs-lookup"><span data-stu-id="45803-113">Then get the [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) interface that enables you to access its methods:</span></span>


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



<span data-ttu-id="45803-114">Analogamente, per ricevere una notifica degli eventi, è necessario implementare l'interfaccia [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) o [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) , creando e registrando un oggetto di quel tipo:</span><span class="sxs-lookup"><span data-stu-id="45803-114">Similarly, to be notified of events, you must implement either the [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) or the [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) interface, creating and registering an object of that type:</span></span>


```
...
// Declare an Agent Notify Sink so that we can get
// notification callbacks from the Agent server.

private AgentNotifySinkEx m_SinkEx = null;
private int            m_SinkID[] = {-1};

public void start()
   {
   ...
   // Create and register a notify sink

   m_SinkEx = new AgentNotifySinkEx();

   m_AgentEx.Register(m_SinkEx, m_SinkID);
   …
   // Give our notify sink access to the character

   m_SinkEx.SetCharacter(m_Merlin[0]);
   ...
   }
```



<span data-ttu-id="45803-115">Per accedere a Microsoft Agent da un'applet Java, è necessario generare le classi Java che si installano con l'applet.</span><span class="sxs-lookup"><span data-stu-id="45803-115">In order to access Microsoft Agent from a Java applet, you must generate Java classes that you install with the applet.</span></span> <span data-ttu-id="45803-116">Per generare questi file, è possibile utilizzare la procedura guidata della libreria dei tipi Java di Visual J++, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="45803-116">You can use the Visual J++ Java Type Library Wizard, for example, to generate these files.</span></span> <span data-ttu-id="45803-117">Se si prevede di ospitare l'applet in una pagina Web, è necessario compilare un pacchetto CAB Java con firma incluso dei file di classe generati che vengono scaricati con la pagina.</span><span class="sxs-lookup"><span data-stu-id="45803-117">If you plan to host the applet on a webpage, you will need to build a signed Java CAB inclusive of the generated class files that download with the page.</span></span> <span data-ttu-id="45803-118">I file di classe sono necessari per accedere al server Microsoft Agent poiché si tratta di un oggetto COM, che viene eseguito all'esterno di Java sandbox.</span><span class="sxs-lookup"><span data-stu-id="45803-118">The class files are necessary to access the Microsoft Agent Server since it is a COM object, that executes outside of the Java sandbox.</span></span> <span data-ttu-id="45803-119">Per ulteriori informazioni sulla sicurezza Trust-Based per Java, vedere <https://www.microsoft.com/java/security> .</span><span class="sxs-lookup"><span data-stu-id="45803-119">To learn more about Trust-Based Security for Java, see <https://www.microsoft.com/java/security>.</span></span>

 

 
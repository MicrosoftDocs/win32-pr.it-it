---
title: Accesso ai servizi tramite Java
description: Accesso ai servizi tramite Java
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a9a3feb1e6cb5fc9ddb8a24b87adfdb42461ebb4581723c1cdb465739c51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976851"
---
# <a name="accessing-services-using-java"></a>Accesso ai servizi tramite Java

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

È anche possibile accedere ai servizi di Microsoft Agent da un'applet Java. Molte delle funzioni accessibili tramite le interfacce di Microsoft Agent restituiscono valori tramite parametri passati per riferimento. Per passare questi parametri da Java, è necessario creare matrici a elemento singolo nel codice e passarli come parametri alla funzione appropriata. Se si usa Microsoft Visual J++ ed è stata eseguita la Creazione guidata libreria dei tipi Java nel server Microsoft Agent, fare riferimento al file summary.txt per verificare quali funzioni richiedono argomenti di matrice. La procedura è simile a quella in C; Si usa [**l'interfaccia IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) per creare un'istanza del server, quindi si carica il carattere :


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



La procedura è leggermente diversa quando si caricano caratteri da una posizione remota HTTP, ad esempio un sito Web. In questo caso il [**metodo Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) è asincrono e genererà un'eccezione COM E \_ PENDING (0x8000000a). Sarà necessario intercettare questa eccezione e gestirla correttamente come avviene nelle funzioni seguenti:


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



Ottenere quindi [**l'interfaccia IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) che consente di accedere ai relativi metodi:


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



Analogamente, per ricevere una notifica degli eventi, è necessario implementare l'interfaccia [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) o [**IAgentNotifySinkEx,**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) creando e registrando un oggetto di quel tipo:


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



Per accedere a Microsoft Agent da un'applet Java, è necessario generare classi Java installate con l'applet. È possibile usare la Creazione guidata libreria dei tipi Java di Visual J++, ad esempio, per generare questi file. Se si prevede di ospitare l'applet in una pagina Web, sarà necessario compilare un file CAB Java firmato che include i file di classe generati che vengono scaricati con la pagina. I file di classe sono necessari per accedere al server Microsoft Agent perché si tratta di un oggetto COM, che viene eseguito all'esterno della sandbox Java. Per altre informazioni su Trust-Based Security per Java, vedere <https://www.microsoft.com/java/security> .

 

 
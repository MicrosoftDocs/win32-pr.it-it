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
# <a name="accessing-services-using-java"></a>Accesso ai servizi tramite Java

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

È anche possibile accedere ai servizi di Microsoft Agent da un'applet Java. Molte delle funzioni accessibili tramite le interfacce di Microsoft Agent restituiscono valori tramite parametri passati per riferimento. Per passare questi parametri da Java, è necessario creare matrici a elemento singolo nel codice e passarle come parametri alla funzione appropriata. Se si utilizza Microsoft Visual J++ ed è stata eseguita la procedura guidata libreria dei tipi Java nel server Microsoft Agent, fare riferimento al file summary.txt per verificare quali funzioni richiedono argomenti di matrice. La procedura è simile a quella in C; usare l'interfaccia [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) per creare un'istanza del server e quindi caricare il carattere:


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



La procedura è leggermente diversa durante il caricamento di caratteri da una posizione remota HTTP, ad esempio un sito Web. In questo caso il metodo [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) è asincrono e genererà un'eccezione com di e \_ in sospeso (0x8000000A). Sarà necessario intercettare questa eccezione e gestirla correttamente, come avviene nelle funzioni seguenti:


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



Ottenere quindi l'interfaccia [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) che consente di accedere ai relativi metodi:


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



Analogamente, per ricevere una notifica degli eventi, è necessario implementare l'interfaccia [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) o [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) , creando e registrando un oggetto di quel tipo:


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



Per accedere a Microsoft Agent da un'applet Java, è necessario generare le classi Java che si installano con l'applet. Per generare questi file, è possibile utilizzare la procedura guidata della libreria dei tipi Java di Visual J++, ad esempio. Se si prevede di ospitare l'applet in una pagina Web, è necessario compilare un pacchetto CAB Java con firma incluso dei file di classe generati che vengono scaricati con la pagina. I file di classe sono necessari per accedere al server Microsoft Agent poiché si tratta di un oggetto COM, che viene eseguito all'esterno di Java sandbox. Per ulteriori informazioni sulla sicurezza Trust-Based per Java, vedere <https://www.microsoft.com/java/security> .

 

 
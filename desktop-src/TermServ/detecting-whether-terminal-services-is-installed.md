---
title: Rilevamento dell'installazione del Servizi Desktop remoto di configurazione
description: Esempio di codice C\ che mostra un metodo che restituisce True se il ruolo del server Servizi Desktop remoto è installato e in esecuzione o false in caso contrario, a partire da Windows Server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf7ac1932c32ea797783d04f4e279bab03339c9b7620c11e72d4b755f084736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871761"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>Rilevamento dell'installazione del Servizi Desktop remoto di configurazione

È possibile usare la classe WMI [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) per rilevare se il Servizi Desktop remoto server è installato.

Nell'esempio C# seguente viene illustrato un metodo che restituisce **True** se il ruolo Servizi Desktop remoto server è installato e in esecuzione o **false** in caso contrario. Poiché la [**classe WMI Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) è disponibile solo a partire da Windows Server 2008, questo codice non è compatibile con le versioni precedenti di Windows.


```CSharp
static void Main(string[] args)
{
    // 14 is the identifier of the Remote Desktop Services role.
    HasServerFeatureById(14);
}

static bool HasServerFeatureById(UInt32 roleId)
{
    try
    {
        ManagementClass serviceClass = new ManagementClass("Win32_ServerFeature");
        foreach (ManagementObject feature in serviceClass.GetInstances())
        {
            if ((UInt32)feature["ID"] == roleId)
            {
                return true;
            }
        }

        return false;
    }
    catch (ManagementException)
    {
        // The most likely cause of this is that this is being called from an 
        // operating system that is not a server operating system.
    }

    return false;
}

```



 

 
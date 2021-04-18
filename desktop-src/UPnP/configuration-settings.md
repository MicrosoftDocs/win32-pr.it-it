---
title: Impostazioni di configurazione
description: Il comportamento dell'API del punto di controllo e dell'API host del dispositivo può essere modificato modificando le impostazioni nel registro di sistema.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297941"
---
# <a name="configuration-settings"></a><span data-ttu-id="270c7-103">Impostazioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="270c7-103">Configuration Settings</span></span>

<span data-ttu-id="270c7-104">Il comportamento dell'API del [punto di controllo](control-point-api.md) e dell' [API host del dispositivo](device-host-api.md) può essere modificato modificando le impostazioni nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="270c7-104">The behavior of the [Control Point API](control-point-api.md) and [Device Host API](device-host-api.md) can be modified by changing settings in the registry.</span></span>

<span data-ttu-id="270c7-105">Sono presenti sette valori del registro di sistema che influiscono sul comportamento:</span><span class="sxs-lookup"><span data-stu-id="270c7-105">There are seven registry values that affect behavior:</span></span>

-   <span data-ttu-id="270c7-106">**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="270c7-106">**DownloadScope**</span></span>
-   <span data-ttu-id="270c7-107">**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="270c7-107">**DeviceLifeTime**</span></span>
-   <span data-ttu-id="270c7-108">\\**Host** \\ dispositivo UPnP **Limite dimensioni file**</span><span class="sxs-lookup"><span data-stu-id="270c7-108">\\**UPnP Device Host**\\**File Size Limit**</span></span>
-   <span data-ttu-id="270c7-109">\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite dimensioni file**</span><span class="sxs-lookup"><span data-stu-id="270c7-109">\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
-   <span data-ttu-id="270c7-110">**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="270c7-110">**MaxCache**</span></span>
-   <span data-ttu-id="270c7-111">**TTL**</span><span class="sxs-lookup"><span data-stu-id="270c7-111">**TTL**</span></span>
-   <span data-ttu-id="270c7-112">**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="270c7-112">**ReceiveScope**</span></span>

<span data-ttu-id="270c7-113">Sono presenti due valori del registro di sistema denominati **limite dimensioni file**, uno per i documenti di descrizione e l'altro per le risposte che usano Simple Object Access Protocol (SOAP).</span><span class="sxs-lookup"><span data-stu-id="270c7-113">There are two registry values called **File Size Limit**, one for description documents and the other for responses that use Simple Object Access Protocol (SOAP).</span></span>

<span data-ttu-id="270c7-114">Il percorso di ognuno dei sette valori nel registro di sistema è il seguente:</span><span class="sxs-lookup"><span data-stu-id="270c7-114">The location of each of the seven values in the registry is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a><span data-ttu-id="270c7-115">Descrizioni del valore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="270c7-115">Registry Value Descriptions</span></span>

<span data-ttu-id="270c7-116">I valori del registro di sistema sono illustrati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="270c7-116">The registry values are explained in the following list.</span></span> <span data-ttu-id="270c7-117">Ogni valore del registro di sistema è **reg \_ DWORD** (un numero intero a 32 bit).</span><span class="sxs-lookup"><span data-stu-id="270c7-117">Each registry value is a **REG\_DWORD** (a 32-bit integer).</span></span> <span data-ttu-id="270c7-118">L'effetto di ogni valore è globale.</span><span class="sxs-lookup"><span data-stu-id="270c7-118">The effect of each value is global.</span></span>

<dl> <dt>

<span data-ttu-id="270c7-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="270c7-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span></span>
</dt> <dd>

<span data-ttu-id="270c7-120">Specifica gli indirizzi IP validi per l'URL del documento di descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="270c7-120">Specifies which IP addresses are valid for the device description document URL.</span></span> <span data-ttu-id="270c7-121">Se l'indirizzo IP dell'host specificato nell'URL del documento di descrizione non è compreso nell'ambito specificato da **DownloadScope**, l'indirizzo IP non è valido e l'oggetto dispositivo non verrà creato.</span><span class="sxs-lookup"><span data-stu-id="270c7-121">If the IP address of the host that is specified in the description document URL is not within the scope specified by **DownloadScope**, that IP address is not valid and the device object will not be created.</span></span>

<span data-ttu-id="270c7-122">I valori validi sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="270c7-122">The valid values are shown in the following table.</span></span> <span data-ttu-id="270c7-123">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="270c7-123">The default value is 1.</span></span>



| <span data-ttu-id="270c7-124">Valore di **DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="270c7-124">Value of **DownloadScope**</span></span> | <span data-ttu-id="270c7-125">Significato</span><span class="sxs-lookup"><span data-stu-id="270c7-125">Meaning</span></span>                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="270c7-126">0</span><span class="sxs-lookup"><span data-stu-id="270c7-126">0</span></span>                          | <span data-ttu-id="270c7-127">L'indirizzo IP dell'host deve essere un indirizzo subnet.</span><span class="sxs-lookup"><span data-stu-id="270c7-127">Host's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="270c7-128">1</span><span class="sxs-lookup"><span data-stu-id="270c7-128">1</span></span>                          | <span data-ttu-id="270c7-129">L'indirizzo IP dell'host deve essere un indirizzo di subnet o un indirizzo privato, ovvero uno dei 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (come specificato da RFC 1918) o 169,254. *x*. *x* (come specificato da RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="270c7-129">Host's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="270c7-130">2</span><span class="sxs-lookup"><span data-stu-id="270c7-130">2</span></span>                          | <span data-ttu-id="270c7-131">L'indirizzo IP dell'host deve essere un indirizzo di subnet, un indirizzo privato o un indirizzo che rientra negli hop TTL (time-to-Live) dal punto di controllo.</span><span class="sxs-lookup"><span data-stu-id="270c7-131">Host's IP address must be a subnet address, private address, or an address that is within the time-to-live (TTL) hops from the control point.</span></span>                                                              |
| <span data-ttu-id="270c7-132">3</span><span class="sxs-lookup"><span data-stu-id="270c7-132">3</span></span>                          | <span data-ttu-id="270c7-133">L'indirizzo IP dell'host può essere qualsiasi indirizzo.</span><span class="sxs-lookup"><span data-stu-id="270c7-133">Host's IP address can be any address.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="270c7-134">>3</span><span class="sxs-lookup"><span data-stu-id="270c7-134">>3</span></span>                      | <span data-ttu-id="270c7-135">Uguale a quello per il valore 0.</span><span class="sxs-lookup"><span data-stu-id="270c7-135">Same as that for the value 0.</span></span>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="270c7-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="270c7-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span></span>
</dt> <dd>

<span data-ttu-id="270c7-137">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="270c7-137">Optional.</span></span> <span data-ttu-id="270c7-138">Specifica la durata, in secondi, del dispositivo che sostituisce il valore specificato nel messaggio di annuncio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="270c7-138">Specifies a device's lifetime, in seconds, which overrides the value provided in the device's announcement message.</span></span> <span data-ttu-id="270c7-139">Se **DeviceLifeTime** è presente, il valore specificato nell'annuncio del dispositivo viene ignorato e viene invece usato il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="270c7-139">If **DeviceLifeTime** is present, the value specified in the device's announcement is ignored and the registry value is used instead.</span></span> <span data-ttu-id="270c7-140">Questo vale per tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="270c7-140">This applies to all devices.</span></span>

<span data-ttu-id="270c7-141">I valori validi sono compresi tra 900 e **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="270c7-141">Valid values range from 900 through **MAX\_DWORD**.</span></span> <span data-ttu-id="270c7-142">Il valore predefinito è 1800.</span><span class="sxs-lookup"><span data-stu-id="270c7-142">The default value is 1800.</span></span> <span data-ttu-id="270c7-143">Se **DeviceLifeTime** è impostato su 0, viene usato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="270c7-143">If **DeviceLifeTime** is set to 0, the default value is used.</span></span>

</dd> <dt>

<span data-ttu-id="270c7-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**Host** \\ dispositivo UPnP **Limite dimensioni file**</span><span class="sxs-lookup"><span data-stu-id="270c7-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP Device Host**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="270c7-145">Specifica la dimensione massima, in byte, di ogni documento di descrizione.</span><span class="sxs-lookup"><span data-stu-id="270c7-145">Specifies the maximum size, in bytes, of each description document.</span></span> <span data-ttu-id="270c7-146">Questa impostazione non è configurabile nelle versioni di Windows precedenti a Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="270c7-146">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="270c7-147">Nelle versioni precedenti questa impostazione è hardcoded come 102400.</span><span class="sxs-lookup"><span data-stu-id="270c7-147">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="270c7-148">I valori validi sono compresi tra 10240 e **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="270c7-148">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="270c7-149">Il valore predefinito è 102400.</span><span class="sxs-lookup"><span data-stu-id="270c7-149">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="270c7-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite dimensioni file**</span><span class="sxs-lookup"><span data-stu-id="270c7-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="270c7-151">Specifica la dimensione massima, in byte, della risposta SOAP accettabile.</span><span class="sxs-lookup"><span data-stu-id="270c7-151">Specifies the maximum size, in bytes, of the SOAP response that is acceptable.</span></span> <span data-ttu-id="270c7-152">Questa impostazione non è configurabile nelle versioni di Windows precedenti a Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="270c7-152">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="270c7-153">Nelle versioni precedenti questa impostazione è hardcoded come 102400.</span><span class="sxs-lookup"><span data-stu-id="270c7-153">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="270c7-154">I valori validi sono compresi tra 10240 e **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="270c7-154">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="270c7-155">Il valore predefinito è 102400.</span><span class="sxs-lookup"><span data-stu-id="270c7-155">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="270c7-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="270c7-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span></span>
</dt> <dd>

<span data-ttu-id="270c7-157">Specifica il numero massimo di voci consentite nella cache Simple Service Discovery Protocol (SSDP).</span><span class="sxs-lookup"><span data-stu-id="270c7-157">Specifies the maximum number of entries allowed in the Simple Service Discovery Protocol (SSDP) cache.</span></span>

<span data-ttu-id="270c7-158">I valori validi sono compresi tra 10 e 30000.</span><span class="sxs-lookup"><span data-stu-id="270c7-158">Valid values range from 10 through 30000.</span></span> <span data-ttu-id="270c7-159">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="270c7-159">The default value is 1000.</span></span>

</dd> <dt>

<span data-ttu-id="270c7-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span><span class="sxs-lookup"><span data-stu-id="270c7-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span></span>
</dt> <dd>

<span data-ttu-id="270c7-161">Specifica la durata (TTL) per un pacchetto SSDP.</span><span class="sxs-lookup"><span data-stu-id="270c7-161">Specifies the time-to-live for an SSDP packet.</span></span> <span data-ttu-id="270c7-162">Ovvero **TTL** specifica il numero di hop consentiti per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="270c7-162">That is, **TTL** specifies the number of hops allowed for a packet.</span></span>

<span data-ttu-id="270c7-163">I valori validi sono compresi tra 1 e 255.</span><span class="sxs-lookup"><span data-stu-id="270c7-163">Valid values range from 1 through 255.</span></span> <span data-ttu-id="270c7-164">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="270c7-164">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="270c7-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="270c7-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span></span>
</dt> <dd>

<span data-ttu-id="270c7-166">Specifica quali indirizzi IP sono origini valide di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="270c7-166">Specifies which IP addresses are valid sources of a message.</span></span> <span data-ttu-id="270c7-167">Se un messaggio in ingresso proviene da un indirizzo non compreso nell'ambito specificato da **ReceiveScope**, il messaggio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="270c7-167">If an incoming message originates from an address that is not within the scope specified by **ReceiveScope**, the message is ignored.</span></span> <span data-ttu-id="270c7-168">Questa impostazione non è configurabile nelle versioni di Windows precedenti a Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="270c7-168">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="270c7-169">Nelle versioni precedenti un messaggio viene accettato indipendentemente dalla relativa origine.</span><span class="sxs-lookup"><span data-stu-id="270c7-169">In the previous versions, a message is accepted without regard to its source.</span></span>

<span data-ttu-id="270c7-170">I valori validi sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="270c7-170">The valid values are shown in the following table.</span></span> <span data-ttu-id="270c7-171">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="270c7-171">The default value is 1.</span></span>



| <span data-ttu-id="270c7-172">Valore di **ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="270c7-172">Value of **ReceiveScope**</span></span> | <span data-ttu-id="270c7-173">Significato</span><span class="sxs-lookup"><span data-stu-id="270c7-173">Meaning</span></span>                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="270c7-174">0</span><span class="sxs-lookup"><span data-stu-id="270c7-174">0</span></span>                         | <span data-ttu-id="270c7-175">L'indirizzo IP del mittente deve essere un indirizzo subnet.</span><span class="sxs-lookup"><span data-stu-id="270c7-175">Sender's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="270c7-176">1</span><span class="sxs-lookup"><span data-stu-id="270c7-176">1</span></span>                         | <span data-ttu-id="270c7-177">L'indirizzo IP del mittente deve essere un indirizzo di subnet o un indirizzo privato, ovvero uno dei 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (come specificato da RFC 1918) o 169,254. *x*. *x* (come specificato da RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="270c7-177">Sender's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="270c7-178">2</span><span class="sxs-lookup"><span data-stu-id="270c7-178">2</span></span>                         | <span data-ttu-id="270c7-179">Non usato.</span><span class="sxs-lookup"><span data-stu-id="270c7-179">Not used.</span></span> <span data-ttu-id="270c7-180">Se **ReceiveScope** è impostato su 2, viene usato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="270c7-180">If **ReceiveScope** is set to 2, the default value is used.</span></span>                                                                                                                                        |
| <span data-ttu-id="270c7-181">3</span><span class="sxs-lookup"><span data-stu-id="270c7-181">3</span></span>                         | <span data-ttu-id="270c7-182">L'indirizzo IP del mittente può essere qualsiasi indirizzo.</span><span class="sxs-lookup"><span data-stu-id="270c7-182">Sender's IP address can be any address.</span></span>                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="270c7-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="270c7-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="270c7-184">Panoramica dell'architettura UPnP</span><span class="sxs-lookup"><span data-stu-id="270c7-184">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 





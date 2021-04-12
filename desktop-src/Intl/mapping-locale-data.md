---
description: NLS include numerose funzioni API che possono essere usate dalle applicazioni per eseguire il mapping dei dati delle impostazioni locali tra gli identificatori delle impostazioni locali e i nomi delle impostazioni locali ed elencare le impostazioni locali non associate ad alcun paese.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Mapping dei dati delle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226452"
---
# <a name="mapping-locale-data"></a>Mapping dei dati delle impostazioni locali

NLS include numerose funzioni API che possono essere usate dalle applicazioni per eseguire il mapping dei dati delle impostazioni locali tra gli [identificatori](locale-identifiers.md) delle impostazioni locali e [i nomi delle impostazioni locali](locale-names.md)ed elencare le impostazioni locali non associate ad alcun paese. In questo argomento viene illustrato l'utilizzo di queste funzioni in Windows Vista e versioni successive e nei sistemi operativi precedenti a Windows Vista (talvolta denominati "sistemi di livello inferiore").

## <a name="map-locale-data-on-windows-vista-and-later"></a>Mappare i dati delle impostazioni locali in Windows Vista e versioni successive

NLS fornisce diverse funzioni di mapping delle impostazioni locali da utilizzare per le applicazioni sviluppate per l'esecuzione in Windows Vista e versioni successive. Sono incluse anche le funzioni che possono essere utilizzate dalle applicazioni per enumerare le impostazioni locali non associate ad alcun paese.

**Usare le funzioni di conversione standard per il mapping dei dati**

Per eseguire il mapping tra un nome delle impostazioni locali e un identificatore delle impostazioni locali, l'applicazione può chiamare la funzione [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) . L'applicazione usa [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) per eseguire il mapping tra un identificatore delle impostazioni locali e un nome delle impostazioni locali.

**Elenca impostazioni locali non associate ad alcun paese**

Per enumerare le impostazioni locali non associate ad alcun paese per Windows 7 e versioni successive, l'applicazione può chiamare [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) con *DwFlags* impostato su [**locale \_ NEUTRALDATA**](locale-neutraldata.md). Può anche usare [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* impostato su [**impostazioni locali \_ INEUTRAL**](locale-ineutral.md).

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>Mappare i dati delle impostazioni locali nei sistemi operativi precedenti a Windows Vista

NLS include una libreria di collegamento diretto (DLL) da usare per le applicazioni sviluppate per l'esecuzione in sistemi operativi precedenti a Windows Vista. La DLL supporta le funzioni di conversione ed elenco per il mapping dei dati.

> [!Note]  
> Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive non devono utilizzare le funzioni di mapping o elenco di livello inferiore.

 

**Usare le funzioni di conversione di livello inferiore per il mapping dei dati**

L'applicazione destinata a un sistema di livello inferiore può chiamare la funzione [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) per convertire un identificatore delle impostazioni locali in un nome delle impostazioni locali. Se è necessario convertire un nome delle impostazioni locali in un identificatore delle impostazioni locali, deve chiamare [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).

**Usare le funzioni elenco di livello inferiore per enumerare le impostazioni locali neutre**

L'applicazione deve chiamare [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) per recuperare l'identificatore delle impostazioni locali dell'elemento padre per le impostazioni locali. Se l'applicazione deve ottenere il nome delle impostazioni locali dell'elemento padre per le impostazioni locali, deve chiamare [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](using-national-language-support.md)
</dt> <dt>

[Identificatori delle impostazioni locali](locale-identifiers.md)
</dt> <dt>

[Nomi delle impostazioni locali](locale-names.md)
</dt> </dl>

 

 




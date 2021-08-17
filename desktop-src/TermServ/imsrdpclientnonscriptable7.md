---
title: Interfaccia IMsRdpClientNonScriptable7
description: Fornisce l'accesso alle proprietà non leggibili della sessione remota di un client nel Desktop remoto ActiveX controllo. Deriva dall'interfaccia IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 01065ef73d1a23f0ac9416a39c4af74042c883e3b4d7f596cb95f6c01043f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941108"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>Interfaccia IMsRdpClientNonScriptable7

Fornisce l'accesso alle proprietà non leggibili della sessione remota di un client nel Desktop remoto ActiveX controllo. Deriva [**dall'interfaccia IMsRdpClientNonScriptable6.**](imsrdpclientnonscriptable6.md) I metodi di questa interfaccia sono accessibili solo tramite vtable. non sono disponibili per l'uso per i client che supportano script.

Un'istanza di questa interfaccia viene ottenuta chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto [**IMsTscAx,**](imstscax-interface.md) passando **\_ IID IMsRdpClientNonScriptable7.**

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientNonScriptable7** eredita da [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable7** include anche questi tipi di membri:

- [Metodi](#methods)
- [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IMsRdpClientNonScriptable7.**


| Metodo            | Descrizione              |
|:------------------|:-------------------------|
| [**DisableDpiCursorScalingForProcess**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  Disabilita il ridimensionamento locale del cursore del mouse ricevuto dal server, assicurando che il rendering della forma del cursore venga eseguito correttamente senza modifiche.                   |

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili **nell'interfaccia IMsRdpClientNonScriptable7.**

| Proprietà         | Tipo di accesso           | Descrizione            |
|:-----------------|:----------------------|:-----------------------|
| [**CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | Sola lettura |  Ottiene la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.   |
| [**Appunti**](imsrdpclientnonscriptable7-clipboard.md)                       | Sola lettura |    Ottiene il controller appunti utilizzato per sincronizzare gli Appunti locali e remoti se la sincronizzazione manuale degli Appunti è abilitata.    |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID MsRdpClient12 è definito come \_ 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> CLSID \_ MsRdpClient12NotSafeForScripting è definito come 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> CLSID MsRdpClient11 è definito come \_ 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> CLSID \_ MsRdpClient11NotSafeForScripting è definito come 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IMsRdpClientNonScriptable7 IID è definito come \_ 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC            |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>

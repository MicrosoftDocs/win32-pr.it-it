---
title: Interfaccia IMsRdpClientNonScriptable7
description: Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303652"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>Interfaccia IMsRdpClientNonScriptable7

Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) . È possibile accedere ai metodi di questa interfaccia solo tramite vtable; non sono disponibili per l'uso nei client con script.

Un'istanza di questa interfaccia viene ottenuta chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto [**IMsTscAx**](imstscax-interface.md) , passando l' **IID \_ IMsRdpClientNonScriptable7**.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientNonScriptable7** eredita da [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable7** dispone anche di questi tipi di membri:

- [Metodi](#methods)
- [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpClientNonScriptable7** dispone di questi metodi.


| Metodo            | Descrizione              |
|:------------------|:-------------------------|
| [**DisableDpiCursorScalingForProcess**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  Disabilita la scalabilità locale del cursore del mouse ricevuta dal server, assicurando che la forma del cursore venga sottoposta a rendering correttamente senza modifiche.                   |

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientNonScriptable7** ha queste proprietà.

| Proprietà         | Tipo di accesso           | Descrizione            |
|:-----------------|:----------------------|:-----------------------|
| [**CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | Sola lettura |  Ottiene la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.   |
| [**Appunti**](imsrdpclientnonscriptable7-clipboard.md)                       | Sola lettura |    Ottiene il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.    |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------|
| Client minimo supportato| Windows 10, versione 1803 (build 17134)      |
| Libreria dei tipi            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID \_ MsRdpClient12 è definito come 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> CLSID \_ MsRdpClient12NotSafeForScripting è definito come 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> CLSID \_ MsRdpClient11 è definito come 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> CLSID \_ MsRdpClient11NotSafeForScripting è definito come 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable7 è definito come 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC            |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>

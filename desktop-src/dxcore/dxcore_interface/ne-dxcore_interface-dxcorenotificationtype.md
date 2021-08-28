---
title: DXCoreNotificationType
description: Definisce le costanti che specificano i tipi di notifiche generate dagli [oggetti IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) [o IDXCoreAdapterList.](./nn-dxcore_interface-idxcoreadapterlist.md)
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 230b6c103f83e72dfe0ba7803cde4b4695a32de724ce44c1aaccf5131d077bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726011"
---
# <a name="dxcorenotificationtype-enum"></a>Enumerazione DXCoreNotificationType

Definisce le costanti che specificano i tipi di notifiche generate dagli [oggetti IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) [o IDXCoreAdapterList.](./nn-dxcore_interface-idxcoreadapterlist.md)

È possibile registrare e annullare la registrazione per queste notifiche chiamando [rispettivamente IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) e [IDXCoreAdapterFactory::UnregisterEventNotification.](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)

## <a name="syntax"></a>Sintassi

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a>Costanti

### <a name="adapterliststale"></a>AdapterListStale

Questa notifica viene generata da un <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">oggetto IDXCoreAdapterList</a> quando l'elenco di adattatori diventa obsoleto. La transizione da aggiornamento a non aggiornamento è unidirele e una sola volta, quindi questa notifica viene generata al massimo una volta.

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

Questa notifica viene generata da un <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">oggetto IDXCoreAdapter</a> quando l'adattatore non è più valido. La transizione da valido a non valido è unidiret e una sola volta, quindi questa notifica viene generata al massimo una volta.

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

Questa notifica viene generata da un oggetto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> quando si verifica una modifica del budget dell'adapter. Questa notifica può verificarsi più volte. L'uso di questa notifica è funzionalmente simile a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent</a>. In risposta a questo evento, è necessario chiamare [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (con [DXCoreAdapterState::AdapterMemoryBudget)](./ne-dxcore_interface-dxcoreadapterstate.md)per valutare lo stato corrente del budget di memoria.

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

Questa notifica viene generata da un <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">oggetto IDXCoreAdapter</a> per notificare la rimozione della protezione del contenuto hardware di un adattatore. Questa notifica può verificarsi più volte. Dal punto di vista funzionale è simile a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a>. In risposta a questo evento, è necessario valutare nuovamente lo stato corrente della sessione di crittografia. ad esempio chiamando [ID3D11VideoContext1::CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) per determinare l'impatto della rimozione dell'hardware per un'interfaccia [ID3D11CryptoSession specifica.](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession)

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Riferimento DXCore](../dxcore-reference.md), Uso [di DXCore](../dxcore-enum-adapters.md) per enumerare gli adapter